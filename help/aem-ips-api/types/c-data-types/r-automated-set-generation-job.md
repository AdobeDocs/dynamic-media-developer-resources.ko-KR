---
description: 자산 핸들 목록 배열을 사용하여 파일을 세트로 그룹화합니다.
solution: Experience Manager
title: AutomatedSetGenerationJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 44df6dfa-1485-40c2-8a14-bbf451b87641
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 3%

---

# AutomatedSetGenerationJob{#automatedsetgenerationjob}

자산 핸들 목록 배열을 사용하여 파일을 세트로 그룹화합니다.

구문

## 매개 변수 {#section-939b2e6946a64238be3709fec2cd0b84}

<table id="table_0E031B2014B646BDA2A94D7E0B55DD5B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이름 </th> 
   <th colname="col2" class="entry"> 유형 </th> 
   <th colname="col3" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:HandleArray</span> </td> 
   <td colname="col3">세트를 만드는 데 사용되는 자산 핸들의 배열입니다. <p>기본적으로 1000은 배열에 포함할 수 있는 최대 자산 수입니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> destFolder</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 세트를 저장할 폴더의 경로입니다. 기본적으로 회사 루트 폴더에 저장합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:부울</span> </td> 
   <td colname="col3"> 자산을 게시해야 하는지 여부를 나타내는 플래그를 설정합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:AutoSetCreationOptions</span> </td> 
   <td colname="col3">업로드한 파일에서 실행할 수 있는 일련의 생성 스크립트입니다. <a href="../../types/c-data-types/r-auto-set-creation-options.md#reference-58b42b39e53345aeb87cd1adc864e7ff" format="dita" scope="local"> AutoSetCreationOptions</a> 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>작업에 대한 자동 이메일 알림을 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**emailSetting 옵션**

`emailSetting` 매개 변수에는 다음 옵션이 포함됩니다.

| 옵션 | 반환 |
|---|---|
| `All` | 지정된 수신자에 대한 모든 작업 알림(오류, 경고, 완료)입니다. |
| `Error` | 지정한 받는 사람에게 작업 오류가 발생합니다. |
| `ErrorAndWarning` | 지정한 수신자에 대한 작업 오류 및 경고 |
| `JobCompletion` | 지정된 수신자에 대한 작업 완료 알림. |
| `None` | 작업이 지정된 받는 사람에게 작업 알림을 보내지 않습니다. |

## 예 {#section-d01ee7671f274a1fa12737e8df91d2cf}

```
<complexType name="AutomatedSetGenerationJob">
  <sequence>
    <element name="assetHandleArray" type="types:HandleArray"/>
    <element name="destFolder" type="xsd:string" minOccurs="0"/>
    <element name="readyForPublish" type="xsd:boolean"/>
    <element name="autoSetCreationOptions" type="types:AutoSetCreationOptions"/>
    <element name="emailSetting" type="xsd:string"/>
  </sequence>
</complexType>
```
