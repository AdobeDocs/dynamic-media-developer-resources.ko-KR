---
description: 자산 검색 문자열, 키워드 및 기타 정보를 가져옵니다. 응답에는 자산에 대한 추가 정보가 포함됩니다.
solution: Experience Manager
title: getSearchStrings
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 16%

---


# getSearchStrings{#getsearchstrings}

자산 검색 문자열, 키워드 및 기타 정보를 가져옵니다. 응답에는 자산에 대한 추가 정보가 포함됩니다.

구문

## 인증된 사용자 유형 {#section-b09c817a59f949a28e1c029e431f5698}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-c1efda4bb15349a68b276bafee8c18fd}

**입력(getSearchStringsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 회사 담당입니다. |
| `*`assetHandle`*` | `xsd:string` | 예 | 자산을 처리합니다. |

**출력(getSearchStringsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`searchStringArray`*` | `types:SearchStrings` | 예 | 자산 검색 문자열의 배열입니다. |

## 예제 {#section-e1f73bff6e4440c489d59cb9aa5384d8}

이 코드 샘플은 자산별 검색 문자열을 반환합니다. 응답에서 빈 배열을 반환합니다.

**요청**

```java
<getSearchStringsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>47</ns1:companyHandle>
   <assetHandle>a|717|1|530</assetHandle>
</getSearchStringsParam>
```

**응답**

없음.
