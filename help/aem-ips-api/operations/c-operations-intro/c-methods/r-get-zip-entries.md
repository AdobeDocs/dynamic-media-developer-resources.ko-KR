---
description: Zip 파일 데이터를 반환합니다.
solution: Experience Manager
title: getZipEntries
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 20%

---


# getZipEntries{#getzipentries}

Zip 파일 데이터를 반환합니다.

구문

## 인증된 사용자 유형 {#section-33a3f03ba8a14086922397619ce12ab8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-aa3f498fe76d4a5f99c42d64520fadce}

**입력(getZipEntriesParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | Zip 파일이 들어 있는 회사의 핸들입니다. |
| `*`assetHandle`*` | `xsd:string` | 예 | Zip 파일을 처리합니다. |

**출력(getZipEntriesReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`zipArray`*` | `types:ZipEntryArray` | 예 | Zip 파일의 항목 배열입니다. |

## 예제 {#section-1fc0ad8fa448492cb5a135d3e3d161ac}

이 코드 샘플은 압축 및 압축 해제된 크기를 포함한 Zip 파일 정보를 반환합니다.

**요청**

```java
<getZipEntriesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetHandle>a|94223|27|30602</assetHandle>
</getZipEntriesParam>
```

**응답**

```java
<getZipEntriesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <zipArray
      <items>
         <name>Checklist_Images/.DS_Store</name>
         <isDirectory>false</isDirectory>
         <lastModified>2007-05-09T15:41:52.000-07:00</lastModified>
         <compressedSize>503</compressedSize>
         <uncompressedSize>6148</uncompressedSize>
      </items>
   ...
   </zipArray>
</getZipEntriesReturn>
```

