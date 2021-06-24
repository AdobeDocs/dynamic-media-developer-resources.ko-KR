---
description: 인쇄 해상도. 응답 이미지에 포함된 인쇄 해상도 값을 무시합니다.
solution: Experience Manager
title: printRes
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 81c4c3b8-946d-401b-a279-ba3f426ea5a4
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---

# printRes{#printres}

인쇄 해상도. 응답 이미지에 포함된 인쇄 해상도 값을 무시합니다.

`printRes= *`val`*`

<table id="simpletable_85C271760AE5466C96115027E6511559"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>인쇄 해상도(dpi)입니다. </p></td> 
 </tr> 
</table>

인쇄 해상도는 일반적으로 카탈로그 항목의 경우 `catalog::PrintResolution`에 의해 정의되며, 그렇지 않으면 원본 이미지에 포함된 인쇄 해상도 값으로 정의됩니다. 템플릿 또는 레이어 복합 이미지의 경우 응답 파일에 포함된 기본 인쇄 해상도는 레이어 이미지의 인쇄 해상도로 가장 낮은 레이어 번호가 있습니다.

인쇄 해상도를 설정하면 회신 이미지의 픽셀 크기가 변경되지 않습니다.

## 속성 {#section-03c7910ebe234804a319e5d0d8ef3a74}

요청 속성입니다. 현재 레이어 설정에 관계없이 적용됩니다.

## 기본값 {#section-d7d89fd235cc418fb381014612530f00}

`catalog::PrintResolution` 원본 이미지에 포함된 인쇄 해상도를 나타냅니다.

## 참조 {#section-4c479b6d6ccd41fc9ce8b239a28e726d}

[카탈로그::PrintResolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5)
