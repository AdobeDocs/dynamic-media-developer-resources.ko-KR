---
description: IPS 웹 서비스는 IPS 웹 서비스 구성 요소가 설치된 IPS 설치에서 액세스하는 WSDL(웹 서비스 설명 언어) 문서 집합에 의해 지원됩니다. 각 IPS API 릴리스에는 버전이 지정된 대상 XML 네임스페이스를 참조하는 새 WSDL 파일이 포함됩니다. 이전 WSDL 네임스페이스 버전도 지원되므로 기존 애플리케이션과의 이전 버전과의 호환성을 유지할 수 있습니다.
solution: Experience Manager
title: IPS 웹 서비스 WSDL 버전
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d7a6079e-286e-4e62-b2ff-551ef4a5815c
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 1%

---

# IPS 웹 서비스 WSDL 버전{#ips-web-service-wsdl-versions}

IPS 웹 서비스는 IPS 웹 서비스 구성 요소가 설치된 IPS 설치에서 액세스하는 WSDL(웹 서비스 설명 언어) 문서 집합에 의해 지원됩니다. 각 IPS API 릴리스에는 버전이 지정된 대상 XML 네임스페이스를 참조하는 새 WSDL 파일이 포함됩니다. 이전 WSDL 네임스페이스 버전도 지원되므로 기존 애플리케이션과의 이전 버전과의 호환성을 유지할 수 있습니다.

## WSDL 액세스 {#section-62e69fa2c87f4dc9bca72f10ba028f6c}

아래 그림과 같이 Scene7 WSDL에 액세스합니다.

```
https://<IPS_hostname:<IPS_port>/<IPS_webapp>/ 
webservice/IpsApi[-<API_version>].wsdl 
```

`<IPS_webapp>`의 기본값은 `scene7`입니다.

**서비스 위치**

서비스 URL은 IPS 웹 서비스 WSDL 문서의 서비스 섹션에 지정됩니다. 서비스 URL은 일반적으로 다음과 같은 형식입니다.

```
https://<IPS_hostname>:<IPS_port>/<IPS_webapp>/ 
services/IpsApiService 
```

**Dynamic Media 영역에 대한 URL에 액세스**

<table id="table_45BB314ABCDA49F38DF7BECF95CC984A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>지리적 위치 </p> </th> 
   <th colname="col2" class="entry"> <p>프로덕션 URL </p> </th> 
   <th colname="col3" class="entry"> <p>스테이징 URL(프로덕션 전 개발 및 테스트에 사용) </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>북미 </p> </td> 
   <td colname="col2"> <p> https://s7sps1apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps1apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>유럽, 중동, 아시아 </p> </td> 
   <td colname="col2"> <p> https://s7sps3apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps3apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>일본/아시아 태평양 </p> </td> 
   <td colname="col2"> <p> https://s7sps5apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps5apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
 </tbody> 
</table>

## 지원되는 WSDL {#section-ebbba69880f94e9c823f1147974eb404}

최신 버전의 IPS API의 기능을 사용하려면 코드를 수정해야 할 수 있습니다. IPS API는 다음 버전에 대한 WSDL을 지원합니다.

<table id="table_6FABCC4E7786448CB56C343E3C0B36CA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>API 릴리스 버전 </p> </th> 
   <th colname="col2" class="entry"> <p>WSDL </p> </th> 
   <th colname="col3" class="entry"> <p>API 네임스페이스 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>6.8/2014R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2014-04-03.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2014-04-03 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.6/2013R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2013-02-15.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2013-02-15 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.0/2012R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2012-02-14.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2012-02-14 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.5 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2010-01-31.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2010-01-31 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.4 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2009-07-31.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2009-07-31 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.2 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2008-09-10.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-09-10 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.0 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2008-01-15.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-01-15 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.0 이전 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

새 기능을 사용하도록 수정해야 하는 기존 애플리케이션은 최신 API 버전으로 업그레이드해야 하며 기존 코드를 변경해야 할 수 있습니다. 자세한 내용은 변경 로그를 참조하십시오.

## SOAP {#section-51e7ecbd1d7f451b9e4f6bf7e1579cae}

**바인딩**

IPS API 웹 서비스는 SOAP 바인딩만 지원합니다.

**지원되는 전송**

IPS API SOAP 바인딩은 HTTP 전송만 지원합니다. HTTPS POST 메서드를 사용하여 모든 SOAP 요청을 수행합니다.

**SOAP 작업 헤더**

요청을 처리하려면 SOAPAction HTTP 헤더를 요청한 작업의 이름으로 설정합니다. WSDL 바인딩 섹션의 작업 이름 특성은 이름을 지정합니다.

**메시지 형식**

document/literal 스타일은 XML 스키마 정의 언어([https://www.w3.org/TR/xmlschema-0/](https://www.w3.org/TR/xmlschema-0/))를 기반으로 하고 WSDL 파일에 지정된 형식의 모든 입력 및 출력 메시지에 사용됩니다. 모든 형식에는 WSDL 파일에 지정된 대상 네임스페이스 값을 사용하여 정규화된 이름이 필요합니다.

**인증 요청**

API 요청에서 인증 자격 증명을 전달하는 기본 방법은 IPS API WSDL에 정의된 대로 `authHeader` 요소를 사용하는 것입니다.

```
<element name="authHeader"> 
    <complexType> 
       <sequence> 
            <element name="user" type="xsd:string"/> 
            <element name="password" type="xsd:string"/> 
            <element name="locale" type="xsd:string" minOccurs="0"/> 
            <element name="appName" type="xsd:string" minOccurs="0"/> 
            <element name="appVersion" type="xsd:string" minOccurs="0"/> 
            <element name="gzipResponse" type="xsd:boolean" minOccurs="0"/> 
            <element name="faultHttpStatusCode" type="xsd:int" minOccurs="0"/> 
       </sequence> 
    </complexType> 
 </element>
```

**필드**

<table id="table_B295FEB0EA584C2BA4122FC084AEF18D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>이름 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 사용자 </span> </p> </td> 
   <td colname="col2"> <p> 유효한 IPS 사용자 이메일입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 암호 </span> </p> </td> 
   <td colname="col2"> <p>사용자 계정 암호. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 로케일 </span> </p> </td> 
   <td colname="col2"> <p> 요청에 대한 선택적 로케일. 자세한 내용은 <b>로케일</b>을(를) 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appName </span> </p> </td> 
   <td colname="col2"> <p> 응용 프로그램 이름을 호출하는 중입니다. 이 매개 변수는 선택 사항이지만 모든 요청에 포함하는 것이 좋습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appVersion </span> </p> </td> 
   <td colname="col2"> <p> 응용 프로그램 버전을 호출하는 중입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gzipResponse </span> </p> </td> 
   <td colname="col2"> <p> 응답 XML의 gzip 압축을 활성화하거나 비활성화하는 선택적 플래그입니다. HTTP Accept-Encoding 헤더가 gzip에 대한 지원을 나타내는 경우 기본적으로 응답은 gzip으로 압축됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> faultHttpStatusCode </span> </p> </td> 
   <td colname="col2"> <p> 오류 응답에 대한 HTTP 상태 코드를 재정의하기 위한 선택적 매개 변수입니다. 기본적으로 오류 응답은 HTTP 상태 코드 500(내부 서버 오류)을 반환합니다. Adobe Flash를 포함한 일부 클라이언트 플랫폼은 상태 코드 200(OK)이 반환되지 않으면 응답 본문을 읽을 수 없습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

`authHeader` 요소는 API 버전에 관계없이 항상 `http://www.scene7.com/IpsApi/xsd` 네임스페이스에 정의되어 있습니다.

다음은 요청 SOAP 헤더에서 `authHeader` 요소를 사용하는 예입니다.

```
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
   <authHeader xmlns="http://www.scene7.com/IpsApi/xsd"> 
      <user>user@scene7.com</user> 
      <password>mypassword</password> 
      <appName>MyApp</appName> 
      <appVersion>1.0</appVersion> 
   </authHeader> 
 </soap:Header>
```

**기타 요청 인증 방법**

어떤 이유로 클라이언트 응용 프로그램에서 `authHeader` SOAP 헤더를 전달할 수 없는 경우 API 요청은 RFC 2617에 지정된 대로 HTTP 기본 인증을 사용하여 자격 증명을 지정할 수도 있습니다.

HTTP 기본 인증을 위해 각 SOAP POST 요청의 HTTP 헤더 섹션에는 다음 형식의 헤더가 포함되어야 합니다.

`Authorization: Basic base64(<IPS_user_email>:<password>)`

`base64()`이(가) 표준 Base64 인코딩을 적용하는 경우 `<IPS_user_email>`은(는) 올바른 IPS 사용자의 전자 메일 주소이고 `<password>`은(는) 사용자 암호입니다.

초기 요청으로 인증 헤더를 선제적으로 전송합니다. 요청에 인증 자격 증명이 포함되지 않은 경우 `IpsApiService`이(가) `401 (Unauthorized)` 상태 코드로 응답하지 않습니다. 대신 `500 (Internal Server Error)`의 상태 코드가 요청을 인증할 수 없다는 SOAP 오류 본문과 함께 반환됩니다.

IPS 3.8 이전에는 SOAP 헤더를 통한 인증이 `AuthUser` 네임스페이스의 `AuthPassword` 및 `http://www.scene7.com/IpsApi` 요소를 사용하여 구현되었습니다. 예:

```
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
   <AuthUser xmlns="http://www.scene7.com/IpsApi">user@scene7.com</AuthUser> 
   <AuthPassword xmlns="http://www.scene7.com/IpsApi">mypassword</AuthPassword> 
</soap:Header>
```

이 스타일은 이전 버전과의 호환성을 위해 계속 지원되지만 `authHeader` 요소를 위해 더 이상 사용되지 않습니다.

**권한 부여 요청**

호출자의 자격 증명이 인증된 후, 호출자가 요청된 작업을 수행할 수 있는 권한이 있는지 확인하기 위해 요청을 검사합니다. 인증은 호출자의 사용자 역할에 기반하며 대상 회사, 대상 사용자 및 기타 운영 매개변수를 확인해야 할 수도 있습니다. 또한 이미지 포털 사용자는 특정 폴더 및 에셋 작업을 수행하는 데 필요한 권한이 있는 그룹에 속해야 합니다. 작업 참조 섹션에서는 각 작업에 대한 인증 요구 사항을 자세히 설명합니다.

**SOAP 요청 및 응답 샘플**

다음 예제에서는 HTTP 헤더를 포함한 전체 `addCompany` 작업을 보여 줍니다.

```
POST /scene7/services/IpsApiService HTTP/1.1 
User-Agent: Axis/2.0 
SOAPAction: addCompany 
Content-Type: text/xml; charset=UTF-8 
 
<?xml version='1.0' encoding='UTF-8'?> 
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"> 
    <soapenv:Header> 
      <authHeader xmlns="http://www.scene7.com/IpsApi/xsd"> 
        <user>user@scene7.com</user> 
        <password>mypassword</password> 
        <appName>MyApp</appName> 
        <appVersion>1.0</appVersion> 
      </authHeader> 
    </soapenv:Header> 
    <soapenv:Body> 
    <ns1:addCompanyParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15"> 
      <ns1:companyName>Sample Company</ns1:companyName> 
      <ns1:expires>2008-07-31T12:00:00-06:00</ns1:expires> 
    </ns1:addCompanyParam> 
    </soapenv:Body> 
 </soapenv:Envelope>
```

그리고 해당 응답은 다음과 같습니다.

```
HTTP/1.1 200 OK 
Server: Apache-Coyote/1.1 
Content-Type: text/xml;charset=UTF-8 
Transfer-Encoding: chunked 
Date: Fri, 21 Jul 2006 20:47:55 GMT 
 
<?xml version='1.0' encoding='utf-8'?><soapenv:Envelope 
xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"> 
   <soapenv:Header /> 
   <soapenv:Body> 
     <ns1:addCompanyReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15"> 
       <ns1:companyInfo> 
          <ns1:companyHandle>2</ns1:companyHandle> 
          <ns1:name>Sample Company</ns1:name> 
          <ns1:rootPath>SampleCompany/</ns1:rootPath> 
          <ns1:expires>2008-07-31T18:00:00.000Z</ns1:expires> 
       </ns1:companyInfo> 
     </ns1:addCompanyReturn> 
   </soapenv:Body> 
</soapenv:Envelope>
```

**SOAP 오류**

작업에 예외 조건이 발생하면 SOAP 오류가 일반적인 응답 대신 SOAP 메시지 본문으로 반환됩니다. 예를 들어 관리자가 아닌 사용자가 이전 `addCompany` 요청을 보내려고 하면 다음 응답이 반환됩니다.

```
HTTP/1.1 500 Internal Server Error 
Server: Apache-Coyote/1.1 
Content-Type: text/xml;charset=UTF-8 
Transfer-Encoding: chunked 
Date: Fri, 21 Jul 2006 16:36:20 GMT 
Connection: close 
 
<?xml version='1.0' encoding='utf-8'?> 
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"> 
   <soapenv:Header /> 
   <soapenv:Body> 
      <soapenv:Fault> 
         <faultcode>soapenv:Client</faultcode> 
         <faultstring>AuthorizationException</faultstring> 
         <detail> 
           <ns1:authorizationFault xmlns:ns1="http://www.scene7.com/IpsApi/xsd"> 
               <code xmlns="http://www.scene7.com/IpsApi/xsd">20003</code> 
             <reason xmlns="http://www.scene7.com/IpsApi/xsd">User does not  
             have permission to access operation 'addCompany'</reason> 
           </ns1:authorizationFault> 
         </detail> 
      </soapenv:Fault> 
   </soapenv:Body> 
</soapenv:Envelope>
```
