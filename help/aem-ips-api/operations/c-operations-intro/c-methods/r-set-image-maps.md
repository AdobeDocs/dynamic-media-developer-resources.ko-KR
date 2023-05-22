---
description: 자산에 대한 이미지 맵을 설정합니다.
solution: Experience Manager
title: 이미지 맵 설정
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0c8e6536-0b9c-4fcc-b71f-511afc670089
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 11%

---

# 이미지 맵 설정{#setimagemaps}

자산에 대한 이미지 맵을 설정합니다.

이미지 맵을 이미 만들었어야 합니다. 이미지 맵은 배열에서 검색한 순서대로 적용됩니다. 이는 제2 이미지 맵이 제1 이미지 맵에 오버레이하고, 제3 이미지 맵이 제2 이미지 맵에 오버레이하는 방식을 의미합니다.

## 승인된 사용자 유형 {#section-adb21c5b679249939dd83816e4a0ee97}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-2292ec1aead947ef8741dd0653a41f42}

**입력(setImageMapsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 회사 핸들. |
| assetHandle | `xsd:string` | 예 | 에셋 핸들. |
| 이미지 맵 배열 | `types:ImageMapDefinitionArray` | 예 | 사전 정의된 이미지 맵 배열입니다. |

**출력(setImageMapsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| imageMapHandleArray | `types:HandleArray` | 예 | 자산에 적용된 이미지 맵 핸들이 있는 배열입니다. |

## 예제 {#section-fe2e35662a6a4ee29cf250c9fd180371}

이 코드 샘플은 이미지 자산에 대한 2개의 이미지 맵을 설정합니다. 이 코드는 이미지 맵을 호출할 때 수행할 모양 유형, 영역 및 작업을 지정합니다. 응답에는 이미지 맵에 대한 핸들이 있는 배열이 포함됩니다.

**요청**

```java
<setImageMapsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|739|1|537</assetHandle>
   <imageMapArray>
      <items>
         <name>ImageMap2</name>
         <shapeType>Rectangle</shapeType>
         <region>40</region>
         <action>400</action>
         <enabled>true</enabled>
      </items>
      <items>
         <name>ImageMap3</name>
         <shapeType>Rectangle</shapeType>
         <region>40</region>
         <action>400</action>
         <enabled>false</enabled>
      </items>
   </imageMapArray>
</setImageMapsParam>
```
