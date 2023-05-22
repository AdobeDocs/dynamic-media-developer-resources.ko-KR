---
description: 모든 회사의 배열을 반환합니다.
solution: Experience Manager
title: getAllCompanies
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0e339ecf-83b5-410c-8683-f3d73bd92339
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 21%

---

# getAllCompanies{#getallcompanies}

모든 회사의 배열을 반환합니다.

구문

## 승인된 사용자 유형 {#section-773db3753b4842e5a4623ad810176508}

* `IpsAdmin`

## 매개 변수 {#section-efd74992e6904ebabe7383b577af4fdb}

**입력(getAllCompaniesParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| includeExpired | `xsd:boolean` | 예 | 만료된 회사와 만료되지 않은 회사를 반환하려면 true로 설정합니다. |

**출력(getAllCompaniesReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| companyArray | `types:CompanyArray` | 예 | 회사의 배열. |

## 예제 {#section-3eecf4e6900b41fb92a0e3214791c6b9}

이 코드 샘플은 IPS에 있는 모든 회사를 배열로 반환합니다. 샘플 응답은 간결성을 위해 잘립니다.

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
