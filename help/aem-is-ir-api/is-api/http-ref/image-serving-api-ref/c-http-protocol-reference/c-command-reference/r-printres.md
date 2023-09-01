---
title: 인쇄 영역
description: 인쇄 해상도. 응답 이미지에 포함된 인쇄 해상도 값을 재정의합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 81c4c3b8-946d-401b-a279-ba3f426ea5a4
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---

# 인쇄 영역{#printres}

인쇄 해상도. 응답 이미지에 포함된 인쇄 해상도 값을 재정의합니다.

`printRes= *`val`*`

<table id="simpletable_85C271760AE5466C96115027E6511559"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>인쇄 해상도(dpi). </p></td> 
 </tr> 
</table>

인쇄 해상도는 일반적으로 다음 방법으로 정의됩니다. `catalog::PrintResolution` 카탈로그 엔트리이면 소스 이미지에 포함된 인쇄 해상도 값으로 표시됩니다. 템플릿 또는 레이어 합성 이미지가 있는 경우 응답 파일에 포함된 기본 인쇄 해상도는 레이어 번호가 가장 낮은 레이어 이미지의 인쇄 해상도입니다.

인쇄 해상도를 설정해도 응답 이미지의 픽셀 크기는 변경되지 않습니다.

## 속성 {#section-03c7910ebe234804a319e5d0d8ef3a74}

요청 속성입니다. 이 설정은 현재 레이어 설정에 관계없이 적용됩니다.

## 기본값 {#section-d7d89fd235cc418fb381014612530f00}

`catalog::PrintResolution`
또는 소스 이미지에 포함된 인쇄 해상도

## 참조 {#section-4c479b6d6ccd41fc9ce8b239a28e726d}

[catalog::PrintResolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5)
