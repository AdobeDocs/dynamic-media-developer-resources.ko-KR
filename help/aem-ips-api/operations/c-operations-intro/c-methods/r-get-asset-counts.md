---
description: 특정 회사와 연결된 자산 및 자산 수를 가져옵니다.
solution: Experience Manager
title: getAssetCounts
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 21cb8023-d6fe-416a-b16f-636df8a37958
TQID: 'https://experienceleague.adobe.com/gvFs-dqQ8oR38MTKrEYaap31BH-MtSaRtGtJd5FO-MY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 141
ht-degree: 9%

---

# getAssetCounts{#getassetcounts}

특정 회사와 연결된 자산 및 자산 수를 가져옵니다.

반환된 `countArray`은(는) 각각 고유한 카운트 필드(데이터 형식 `xsd:int`)가 있는 `assetTypes`(데이터 형식 `xsd:string`)의 배열로 구성되어 배열의 요소당 여러 자산 형식을 표시할 수 있습니다.구문

## 승인된 사용자 유형 {#section-6234754722184e828352f10eb18fbce9}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-2a9581315eca427d8a3d26cc3fca7b1f}

**입력(getAssetCountsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 계산하려는 자산이 있는 회사에 대한 핸들입니다. |

**출력(getAssetCountsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| countArray | `types:AssetCountArray` | 아니요 | 에셋 유형의 배열로, 각 배열에는 자체 카운트 필드가 있으며 배열의 요소당 여러 에셋 유형을 표시할 수 있습니다. |

## 예제 {#section-6052a503eb3843f6adb99e200fdba280}

이 코드 샘플은 자산 수를 가져오기 위해 회사의 핸들을 IPS 웹 서비스 서버로 보낸 `getAssetCountsParam`의 필드로 사용합니다.

**요청**

```java
<getAssetCountsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
</getAssetCountsParam>
```

**응답**

```java
<getAssetCountsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <countArray>
      <items>
         <assetType>Image</assetType>
         <count>44</count>
      </items>
      <items>
         <assetType>Flash</assetType>
         <count>3</count>
      </items>
   </countArray>
</getAssetCountsReturn>
```

