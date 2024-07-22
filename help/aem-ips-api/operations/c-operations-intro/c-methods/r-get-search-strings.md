---
description: 검색 문자열, 키워드 및 자산에 대한 기타 정보를 가져옵니다. 응답에는 자산에 대한 추가 정보가 포함됩니다.
solution: Experience Manager
title: getSearchStrings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e94215b8-1121-4be6-a8a9-e9444c57495d
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 15%

---

# getSearchStrings{#getsearchstrings}

검색 문자열, 키워드 및 자산에 대한 기타 정보를 가져옵니다. 응답에는 자산에 대한 추가 정보가 포함됩니다.

구문

## 승인된 사용자 유형 {#section-b09c817a59f949a28e1c029e431f5698}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-c1efda4bb15349a68b276bafee8c18fd}

**입력(getSearchStringsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 회사를 위해 처리하십시오. |
| assetHandle | `xsd:string` | 예 | 자산을 처리합니다. |

**출력(getSearchStringsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| 검색 문자열 배열 | `types:SearchStrings` | 예 | 에셋 검색 문자열의 배열입니다. |

## 예제 {#section-e1f73bff6e4440c489d59cb9aa5384d8}

이 코드 샘플은 자산별 검색 문자열을 반환합니다. 응답이 빈 배열을 반환합니다.

**요청**

```java
<getSearchStringsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>47</ns1:companyHandle>
   <assetHandle>a|717|1|530</assetHandle>
</getSearchStringsParam>
```

**응답**

없음.
