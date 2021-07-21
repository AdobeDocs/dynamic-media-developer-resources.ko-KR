---
description: 자산에 대한 이미지 맵을 설정합니다.
solution: Experience Manager
title: setImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0c8e6536-0b9c-4fcc-b71f-511afc670089
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 10%

---

# setImageMap{#setimagemaps}

자산에 대한 이미지 맵을 설정합니다.

이미지 맵을 이미 만들었어야 합니다. 이미지 맵은 배열에서 검색 순서로 적용됩니다. 즉, 두 번째 이미지 맵은 첫 번째, 세 번째 이미지 맵은 두 번째 오버레이 등을 오버레이합니다.

## 인증된 사용자 유형 {#section-adb21c5b679249939dd83816e4a0ee97}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-2292ec1aead947ef8741dd0653a41f42}

**입력(setImageMapParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 회사 핸들. |
| `*`assetHandle`*` | `xsd:string` | 예 | 자산 핸들. |
| `*`imageMapArray`*` | `types:ImageMapDefinitionArray` | 예 | 사전 정의된 이미지 맵의 배열입니다. |

**출력(setImageMapReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`imageMapHandleArray`*` | `types:HandleArray` | 예 | 이미지 맵 핸들이 자산에 적용된 배열입니다. |

## 예제 {#section-fe2e35662a6a4ee29cf250c9fd180371}

이 코드 샘플은 이미지 자산에 대한 2개의 이미지 맵을 설정합니다. 이 코드는 이미지 맵을 호출할 때 취하는 모양 유형, 영역 및 작업을 지정합니다. 응답에는 이미지 맵에 대한 핸들이 있는 배열이 포함되어 있습니다.

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
