---
description: 모든 회사의 배열을 반환합니다.
solution: Experience Manager
title: getAllCompany
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 19%

---


# getAllCompanies{#getallcompanies}

모든 회사의 배열을 반환합니다.

구문

## 인증된 사용자 유형 {#section-773db3753b4842e5a4623ad810176508}

* `IpsAdmin`

## 매개 변수 {#section-efd74992e6904ebabe7383b577af4fdb}

**입력(getAllCompanyParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`includeExpired`*` | `xsd:boolean` | 예 | 만료되거나 만료되지 않은 회사를 반환하려면 true로 설정합니다. |

**출력(getAllCompanyReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyArray`*` | `types:CompanyArray` | 예 | 기업 배열입니다. |

## 예제 {#section-3eecf4e6900b41fb92a0e3214791c6b9}

이 코드 샘플은 배열에 있는 IPS의 모든 회사를 반환합니다. 참고: 샘플 응답은 간결성에 대해 잘립니다.

**요청**

```java
<ns1:getAllCompaniesParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:includeExpired>false</ns1:includeExpired>
</ns1:getAllCompaniesParam>
```

**응답**

```java
<ns1:getAllCompaniesReturnxmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyArray>
      <ns1:items>
         <ns1:companyHandle>18</ns1:companyHandle>
         <ns1:name>00webload</ns1:name>
         <ns1:rootPath>00webload/</ns1:rootPath>
         <ns1:expires>2101-02-01T07:00:00.667Z</ns1:expires>
      </ns1:items>
      <ns1:items>
         <ns1:companyHandle>19</ns1:companyHandle>
         <ns1:name>01webload</ns1:name>
         <ns1:rootPath>01webload/</ns1:rootPath>
         <ns1:expires>2101-02-01T07:00:00.414Z</ns1:expires>
      </ns1:items>
      . . .
   </ns1:companyArray>
</ns1:getAllCompaniesReturn>
```

