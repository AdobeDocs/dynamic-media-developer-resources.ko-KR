---
description: 명명된 Photoshop 경로를 둘러싸는 사각형의 좌표를 반환합니다.
solution: Experience Manager
title: getPhotoshopPath
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 46d88547-bb60-4370-9c79-bd281b40ba28
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 19%

---

# getPhotoshopPath{#getphotoshoppath}

명명된 Photoshop 경로를 둘러싸는 사각형의 좌표를 반환합니다.

구문

## 승인된 사용자 유형 {#section-c417a287612847cb98dd0aa9c67fd78a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* &quot;

## 매개 변수 {#section-ebffe496284c4ced9f329f78127be199}

**입력(getPhotoshopPathParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 작업하려는 이미지로 회사를 처리합니다. |
| assetHandle | `xsd:string` | 예 | 이미지 에셋에 대해 처리합니다. |
| pathName | `xsd:string` | 예 | 반환할 Photoshop 경로의 이름입니다. |

**출력(getPhotoshopPathReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| perspectiveQuad | `types:PerspectiveQuad` | 예 | 경로를 기반으로 이미지 좌표를 반환합니다. 다음을 참조하십시오 [PerspectiveQuad](../../../types/c-data-types/r-perspective-quad.md#reference-3c1f780f9c264e5b870b1ade24566204). |

## 예제 {#section-1f0461cbdc184c8d8925336d5279db47}

**요청**

```java
<getPhotoshopPathParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <companyHandle>c|301</companyHandle>
  <assetHandle>a|26014</assetHandle>
  <pathName>Face Path</pathName>
</getPhotoshopPathParam>
```

**응답**

```java
<getPhotoshopPathReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <perspectiveQuad>
    <x0>932.19</x0>
    <y0>296.592</y0>
    <x1>968.769</x1>
    <y1>320.16</y1>
    <x2>1119.56</x2>
    <y2>1200.0</y2>
    <x3>900.43</x3>
    <y3>1200.0</y3>
  </perspectiveQuad>
</getPhotoshopPathReturn>
```

>[!MORELIKETHIS]
>
>* [PerspectiveQuad](../../../types/c-data-types/r-perspective-quad.md#reference-3c1f780f9c264e5b870b1ade24566204)

