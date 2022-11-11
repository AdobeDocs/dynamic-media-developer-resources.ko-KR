---
title: HTTP POST를 통해 UploadFile 서블릿에 자산 업로드
description: 에 자산 업로드 [!DNL Dynamic Media] Classic에는 업로드된 파일과 연관된 모든 로그 활동을 조정하는 작업을 설정하는 하나 이상의 HTTP POST 요청이 포함됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: e40293be-d00f-44c1-8ae7-521ce3312ca8
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 3%

---

# HTTP POST를 통해 UploadFile 서블릿에 자산 업로드{#uploading-assets-by-way-of-http-posts-to-the-uploadfile-servlet}

Dynamic Media Classic에 자산 업로드에는 업로드된 파일과 연관된 모든 로그 활동을 조정하는 작업을 설정하는 하나 이상의 HTTP POST 요청이 포함됩니다.

다음 URL을 사용하여 UploadFile 서블릿에 액세스합니다.

```
https://<server>/scene7/UploadFile
```

>[!NOTE]
>
>업로드 작업에 대한 모든 POST 요청은 동일한 IP 주소에서 발생해야 합니다.

**Dynamic Media 지역의 URL 액세스**

<table id="table_45BB314ABCDA49F38DF7BECF95CC984A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>지리적 위치 </p> </th> 
   <th colname="col2" class="entry"> <p>프로덕션 URL </p> </th> 
   <th colname="col3" class="entry"> <p>스테이징 URL(사전 프로덕션 개발 및 테스트에 사용) </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>북미 </p> </td> 
   <td colname="col2"> <p> https://s7sps1ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps1ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>유럽, 중동, 아시아 </p> </td> 
   <td colname="col2"> <p> https://s7sps3ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps3ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>일본/아시아 태평양 </p> </td> 
   <td colname="col2"> <p> https://s7sps5ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps5ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
 </tbody> 
</table>

## 업로드 작업의 워크플로우 {#section-873625b9512f477c992f5cdd77267094}

업로드 작업은 일반을 사용하는 하나 이상의 HTTP POST로 구성됩니다 `jobHandle` 처리를 동일한 작업에 상호 연관시킬 수 있습니다. 각 요청은 `multipart/form-data` 인코딩되고 다음 양식 부분으로 구성됩니다.

>[!NOTE]
>
>업로드 작업에 대한 모든 POST 요청은 동일한 IP 주소에서 발생해야 합니다.

|  HTTP POST 양식 파트  |  설명  |
|---|---|
| `auth`  |   필수. 인증 및 클라이언트 정보를 지정하는 XML authHeader 문서입니다. 자세한 내용은 **인증 요청** 아래에 [SOAP](/help/aem-ips-api/c-wsdl-versions.md). |
| `file params`  |   선택 사항입니다. 각 POST 요청에 업로드할 파일을 하나 이상 포함할 수 있습니다. 각 파일 부분에는 없는 경우 IPS의 대상 파일 이름으로 사용되는 Content-Disposition 헤더에 파일 이름 매개 변수가 포함될 수 있습니다 `uploadPostParams/fileName` 매개 변수가 지정되었습니다. |

|  HTTP POST 양식 파트   |  uploadPostParams 요소 이름   |  유형   |  설명   |
|---|---|---|---|
| `uploadParams` (필수. XML `uploadParams` 업로드 매개 변수 지정 문서)   |   `companyHandle`  |  `xsd:string`  | 필수. 파일을 업로드할 회사를 처리합니다.  |
| `uploadParams` (필수. XML `uploadParams` 업로드 매개 변수 지정 문서) | `jobName`  |  `xsd:string`  | 다음 중 하나 `jobName` 또는 `jobHandle` 는 필수입니다. 업로드 작업의 이름입니다.  |
| `uploadParams` (필수. XML `uploadParams` 업로드 매개 변수 지정 문서) | `jobHandle`  |  `xsd:string`  | 다음 중 하나 `jobName` 또는 `jobHandle` 는 필수입니다. 이전 요청에서 시작된 업로드 작업을 처리합니다.  |
| `uploadParams` (필수. XML `uploadParams` 업로드 매개 변수 지정 문서) | `locale`  |  `xsd:string`  | 선택 사항입니다. 지역화를 위한 언어 및 국가 코드입니다.  |
| `uploadParams` (필수. XML `uploadParams` 업로드 매개 변수 지정 문서) | `description`  |  `xsd:string`  | 선택 사항입니다. 작업에 대한 설명입니다.  |
| `uploadParams` (필수. XML `uploadParams` 업로드 매개 변수 지정 문서) | `destFolder`  |  `xsd:string`  | 선택 사항입니다. 파일 이름 속성에 접두사를 추가할 Target 폴더 경로, 특히 파일 이름의 전체 경로를 지원하지 않을 수 있는 브라우저 및 기타 클라이언트의 경우  |
| `uploadParams` (필수. XML `uploadParams` 업로드 매개 변수 지정 문서) | `fileName`  |  `xsd:string`  | 선택 사항입니다. 대상 파일의 이름입니다. 파일 이름 속성을 무시합니다. |
| `uploadParams` (필수. XML `uploadParams` 업로드 매개 변수 지정 문서) | `endJob`  |  `xsd:boolean`  | 선택 사항입니다. 기본값은 false입니다. |
| `uploadParams` (필수. XML `uploadParams` 업로드 매개 변수 지정 문서) | `uploadParams`  |  `types:UploadPostJob`  | 기존 활성 작업에 대한 후속 요청인 경우 선택 사항입니다. 기존 작업이 있다면 `uploadParams` 이 무시되고 기존 작업 업로드 매개 변수가 사용됩니다. 자세한 내용은 [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4) |

내 `<uploadPostParams>` 블록은 `<uploadParams>` 포함된 파일의 처리를 지정하는 블록입니다.

자세한 내용은 [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4).

당신이 만약 `uploadParams` 개별 파일에 대해 동일한 작업의 일부로 매개 변수를 변경할 수 있지만 그렇지 않습니다. 동일한 항목 사용 `uploadParams` 전체 작업에 대한 매개 변수입니다.

새 업로드 작업에 대한 초기 POST 요청에는 `jobName` 매개 변수, 바람직하게는 고유한 작업 이름을 사용하여 후속 작업 상태 폴링 및 작업 로그 쿼리를 단순화합니다. 동일한 업로드 작업에 대한 추가 POST 요청에서는 `jobHandle` 매개 변수 대신 `jobName`를 사용 `jobHandle` 초기 요청에서 반환된 값입니다.

업로드 작업에 대한 최종 POST 요청은 `endJob` 이 작업에 대해 이후의 파일이 POSTed가 되지 않도록 매개 변수를 true로 설정합니다. 이렇게 하면 모든 POSTed 파일을 수집한 후 즉시 작업을 완료할 수 있습니다. 그렇지 않으면 30분 내에 추가 POST 요청을 받지 못하면 작업이 시간 초과됩니다.

## UploadPOST 응답 {#section-421df5cc04d44e23a464059aad86d64e}

성공적인 POST 요청의 경우 응답 본문은 XML입니다 `uploadPostReturn` XSD가 지정하는 대로 문서에 지정된 경우

```xml {.line-numbers}
<element name="uploadPostReturn"> 
        <complexType> 
            <sequence> 
                <element name="jobHandle" type="xsd:string"/> 
            </sequence> 
        </complexType> 
    </element>
```

다음 `jobHandle` 반환된 가 `uploadPostParams`/ `jobHandle` 동일한 작업에 대한 후속 POST 요청에 대한 매개 변수입니다. 이 데이터를 사용하여 작업 상태를 `getActiveJobs` 작업 또는 작업 로그를 `getJobLogDetails` 작업.

POST 요청을 처리하는 동안 오류가 발생하면 응답 본문은 에 설명된 대로 API 오류 유형 중 하나로 구성됩니다 [장애](faults/c-faults/c-faults.md#concept-28c5e495f39443ecab05384d8cf8ab6b).

## POST 요청 예 {#section-810fe32abdb9426ba0fea488dffadd1e}

```{.line-numbers}
POST /scene7/UploadFile HTTP/1.1 
User-Agent: Jakarta Commons-HttpClient/3.1 
Host: localhost 
Content-Length: 362630 
Content-Type: multipart/form-data; boundary=O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
  
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
Content-Disposition: form-data; name="auth" 
Content-Type: text/plain; charset=US-ASCII 
Content-Transfer-Encoding: 8bit 
  
            <authHeader xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03">  
                   <user>sampleuser@test.com</user>  
                   <password>*</password>  
                   <locale>en-US</locale>  
                   <appName>MyUploadServletTest</appName>  
                   <appVersion>1.0</appVersion>  
                   <faultHttpStatusCode>200</faultHttpStatusCode>  
           </authHeader>                   
        
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
Content-Disposition: form-data; name="uploadParams" 
Content-Type: text/plain; charset=US-ASCII 
Content-Transfer-Encoding: 8bit 
  
            <uploadPostParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
                <companyHandle>c|2101</companyHandle> 
                <jobName>uploadFileServlet-1376682217351</jobName> 
                <uploadParams> 
                    <overwrite>true</overwrite> 
                    <readyForPublish>true</readyForPublish> 
                    <preservePublishState>true</preservePublishState> 
                    <createMask>true</createMask> 
                    <preserveCrop>true</preserveCrop> 
                    <manualCropOptions> 
                      <left>500</left> 
                      <right>500</right> 
                      <top>500</top> 
                      <bottom>500</bottom> 
                    </manualCropOptions> 
                    <photoshopOptions> 
                      <process>MaintainLayers</process> 
                      <layerOptions> 
                        <layerNaming>AppendNumber</layerNaming> 
                        <anchor>Northwest</anchor> 
                        <createTemplate>true</createTemplate> 
                        <extractText>true</extractText> 
                        <extendLayers>false</extendLayers> 
                      </layerOptions> 
                    </photoshopOptions> 
                    <emailSetting>None</emailSetting> 
                </uploadParams> 
            </uploadPostParam>        
        
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ-- 
Content-Disposition: form-data; name="file1"; filename="ApiTestCo1/UploadFileServlet1376682217351//1376682217351-1.jpg" 
Content-Type: application/octet-stream; charset=ISO-8859-1 
Content-Transfer-Encoding: binary 
<file bytes ... > 
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ-- 
Content-Disposition: form-data; name="file2"; filename="ApiTestCo1/UploadFileServlet1376682217351//1376682217351-2.jpg" 
Content-Type: application/octet-stream; charset=ISO-8859-1 
Content-Transfer-Encoding: binary 
<file bytes ... > 
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ--
```

## POST 응답 예 - 성공 {#section-0d515ba14c454ed0b5196ac8d1bb156e}

```{.line-numbers}
HTTP/1.1 200 OK 
Content-Type: text/xml;﻿charset=utf-8 
Content-Length: 204 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
'1.0' encoding='UTF-8'?><uploadPostReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <jobHandle>j|2101||uploadFileServlet-1376682217351|54091</jobHandle> 
</uploadPostReturn>
```

## POST 응답 예 - 오류 {#section-efc32bb371554982858b8690b05090ec}

```{.line-numbers}
HTTP/1.1 200 OK 
Content-Type: text/xml;charset=utf-8 
Content-Length: 210 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
<?xml version='1.0' encoding='UTF-8'?><tns:authenticationFault xmlns:tns="http://www.scene7.com/IpsApi/xsd"><tns:code>10001</tns:code><tns:reason>Invalid username/password</tns:reason></tns:authenticationFault> 
 
```
