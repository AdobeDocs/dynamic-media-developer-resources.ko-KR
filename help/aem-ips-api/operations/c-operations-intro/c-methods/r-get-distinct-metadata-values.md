---
description: 메타데이터 필드에 대한 모든 값을 반환합니다.
solution: Experience Manager
title: getDistinctMetadataValues
feature: Dynamic Media Classic,SDK/API,메타데이터
role: Developer,Administrator
exl-id: 1987d8b0-64e4-49be-af45-98e4c6542e5f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 22%

---

# getDistinctMetadataValues{#getdistinctmetadatavalues}

메타데이터 필드에 대한 모든 값을 반환합니다.

구문

## 인증된 사용자 유형 {#section-f0f44fdcb318490582dd04de8eaf745d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-600f36a32ff147cb83149943d37843e2}

**입력(getDistinctMetadataValuesParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 데이터를 가져올 회사의 핸들입니다. |
| `*`metadataKey`*` | `xsd:string` | 예 | 점 표기법의 메타데이터 키. |

**출력(getDistinctMetadataValuesReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`valueArray`*` | `types:ValueArray` | 예 | 요청된 메타데이터 필드의 값입니다. |

## 예제 {#section-0189fa6fb31646cda5ce1b0bc4fcdf46}

**요청**

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:xsd="http://www.scene7.com/IpsApi/xsd"
xmlns:ns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <soapenv:Header>
      <xsd:authHeader>
         <xsd:user>user@company.com</xsd:user>
         <xsd:password>password</xsd:password>
      </xsd:authHeader>
   </soapenv:Header>
   <soapenv:Body>
   <ns:getDistinctMetadataValuesParam>
      <ns:companyHandle>680</ns:companyHandle>
      <ns:metadataKey>dc.format</ns:metadataKey>
      </ns:getDistinctMetadataValuesParam>
   </soapenv:Body>
</soapenv:Envelope>
```

**응답**

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/">
   <soapenv:Body>
      <getDistinctMetadataValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
         <valueArray>
            <items>
               <value>N/A</value>
               <count>412</count>
            </items>
            <items>
               <value>image/jpeg</value>
               <count>189</count>
            </items>
            <items>
               <value>image/epsf</value>
               <count>1</count>
            </items>
            <items>
               <value>image/tiff</value>
               <count>3</count>
            </items>
         </valueArray>
      </getDistinctMetadataValuesReturn>
   </soapenv:Body>
</soapenv:Envelope>
```
