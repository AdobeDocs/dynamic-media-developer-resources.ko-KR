---
description: 특정 회사와 연결된 자산 및 자산 수를 가져옵니다.
seo-description: 특정 회사와 연결된 자산 및 자산 수를 가져옵니다.
seo-title: getAssetCounts
solution: Experience Manager
title: getAssetCounts
topic: Scene7 Image Production System API
uuid: 92103806-59da-444f-b69c-d045d0ebf42e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getAssetCounts{#getassetcounts}

특정 회사와 연결된 자산 및 자산 수를 가져옵니다.

반환된 `countArray` 항목은 `assetTypes` (데이터 유형 `xsd:string`) 배열로 구성되며 각각 자체 카운트 필드(데이터 유형 `xsd:int`)가 있으므로 배열의 요소당 여러 자산 유형을 표현할 수 있습니다.
구문

## 인증된 사용자 유형 {#section-6234754722184e828352f10eb18fbce9}

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
| ` *`companyHandle`*` | `xsd:string` | 예 | 카운트할 자산이 있는 회사의 핸들. |

**출력(getAssetCountsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`countArray`*` | `types:AssetCountArray` | 아니요 | 자체 카운트 필드가 있는 자산 유형의 배열으로서, 배열의 요소당 여러 자산 유형을 표현할 수 있습니다. |

## 예제 {#section-6052a503eb3843f6adb99e200fdba280}

이 코드 샘플에서는 IPS 웹 서비스 서버로 `getAssetCountsParam` 보내진 회사의 핸들을 필드로 사용하여 자산 수를 가져옵니다.

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

