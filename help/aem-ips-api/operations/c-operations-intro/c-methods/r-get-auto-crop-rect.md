---
description: 배경색 또는 투명도를 기반으로 이미지에 대해 잘린 영역을 반환합니다.
solution: Experience Manager
title: getAutoCropRect
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e291597a-b863-42dd-88dc-13398b734410
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 15%

---

# getAutoCropRect{#getautocroprect}

배경색 또는 투명도를 기반으로 이미지에 대해 잘린 영역을 반환합니다.

구문

## 인증된 사용자 유형 {#section-32dfe7bb68764b93ae01e05ff7a7bdd0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-965d5973b8344d43a74b3e07cf0b7eb3}

**입력(getAutoCropRectParam)**

>[!NOTE]
>
>이 메서드를 호출할 때 autoColorCropOptions 또는 autoTransparentCropOptions를 지정하십시오.

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| companyHandle | `xsd:string` | 예 | 작업할 자산이 있는 회사의 핸들입니다. |
| assetHandle | `xsd:string` | 예 | 작업할 자산의 핸들입니다. |
| autoColorCropOptions | `types:AutoColorCropOptions` | 아니요 | 색상을 기반으로 자르기 사각형을 계산합니다. 자세한 내용은 [자동 색상 자르기 옵션](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6). |
| autoTransparentCropOptions | `types:AutoTransparentCropOptions` | 아니요 | 투명도를 기반으로 자르기 사각형을 계산합니다. 자세한 내용은 [자동 투명 자르기 옵션](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b). |

**출력(getAutoCropRectReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| xOffset | `xsd:int` | 예 | 계산된 자르기 영역의 시작 왼쪽 픽셀 좌표입니다. |
| yOffset | `xsd:int` | 예 | 계산된 자르기 영역의 시작 위쪽 픽셀 좌표입니다. |
| 너비 | `xsd:int` | 예 | 계산된 자르기 영역의 폭(픽셀 단위)입니다. |
| 높이 | `xsd:int` | 예 | 계산된 자르기 영역의 높이(픽셀 단위)입니다. |

## 예제 {#section-ba65bd66086d491cad1cea535954ee1f}

**요청**

```java
<getAutoCropRectParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31-beta">
  <companyHandle>c|3578</companyHandle>
  <assetHandle>a|3192146</assetHandle>
  <autoColorCropOptions>
    <corner>UpperLeft</corner>
    <tolerance>0.5</tolerance>
  </autoColorCropOptions>
</getAutoCropRectParam>
```

**응답**

```java
<getAutoCropRectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31-beta">
  <xOffset>452</xOffset>
  <yOffset>66</yOffset>
  <width>1271</width>
  <height>1874</height>
</getAutoCropRectReturn>
```

>[!MORELIKETHIS]
>
>* [자동 색상 자르기 옵션](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6)
>* [자동 투명 자르기 옵션](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b)

