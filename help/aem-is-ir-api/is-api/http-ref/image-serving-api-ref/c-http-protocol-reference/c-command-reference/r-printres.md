---
description: 인쇄 해상도. 응답 이미지에 포함된 인쇄 해상도 값을 무시합니다.
solution: Experience Manager
title: printRes
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 3%

---


# printRes{#printres}

인쇄 해상도. 응답 이미지에 포함된 인쇄 해상도 값을 무시합니다.

`printRes= *`val`*`

<table id="simpletable_85C271760AE5466C96115027E6511559"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>인쇄 해상도(dpi). </p></td> 
 </tr> 
</table>

인쇄 해상도는 카탈로그 항목의 경우 일반적으로 `catalog::PrintResolution`에 의해 정의되며, 그렇지 않은 경우에는 소스 이미지에 포함된 인쇄 해상도 값으로 정의됩니다. 템플릿 또는 레이어로 구성된 합성 이미지의 경우 응답 파일에 포함된 기본 인쇄 해상도는 레이어 번호가 가장 낮은 레이어 이미지의 인쇄 해상도입니다.

인쇄 해상도를 설정해도 회신 이미지의 픽셀 크기는 변경되지 않습니다.

## 속성 {#section-03c7910ebe234804a319e5d0d8ef3a74}

요청 속성을 참조하십시오. 현재 레이어 설정에 관계없이 적용됩니다.

## 기본값 {#section-d7d89fd235cc418fb381014612530f00}

`catalog::PrintResolution` 소스 이미지에 임베드된 인쇄 해상도입니다.

## 참조 {#section-4c479b6d6ccd41fc9ce8b239a28e726d}

[카탈로그::PrintResolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5)
