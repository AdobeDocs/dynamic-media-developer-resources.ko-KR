---
title: 인쇄 영역
description: 인쇄 해상도. 응답 이미지에 포함된 인쇄 해상도 값을 재정의합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 81c4c3b8-946d-401b-a279-ba3f426ea5a4
TQID: 'https://experienceleague.adobe.com/QJMoF8XW-O1W-E12Cpix3uiwiqKOFo6A4bI6I0hv0II'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 2%

---

# 인쇄 영역{#printres}

인쇄 해상도. 응답 이미지에 포함된 인쇄 해상도 값을 재정의합니다.

`printRes= *`val`*`

<table id="simpletable_85C271760AE5466C96115027E6511559"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 값</span> </p> </td> 
  <td class="stentry"> <p>인쇄 해상도(dpi). </p></td> 
 </tr> 
</table>

인쇄 해상도는 일반적으로 카탈로그 항목인 경우 `catalog::PrintResolution`에 의해 정의되며, 그렇지 않은 경우 소스 이미지에 포함된 인쇄 해상도 값에 의해 정의됩니다. 템플릿 또는 레이어 합성 이미지가 있는 경우 응답 파일에 포함된 기본 인쇄 해상도는 레이어 번호가 가장 낮은 레이어 이미지의 인쇄 해상도입니다.

인쇄 해상도를 설정해도 응답 이미지의 픽셀 크기는 변경되지 않습니다.

## 속성 {#section-03c7910ebe234804a319e5d0d8ef3a74}

요청 속성입니다. 이 설정은 현재 레이어 설정에 관계없이 적용됩니다.

## 기본값 {#section-d7d89fd235cc418fb381014612530f00}

`catalog::PrintResolution`
또는 소스 이미지에 포함된 인쇄 해상도

## 참조 {#section-4c479b6d6ccd41fc9ce8b239a28e726d}

[catalog::PrintResolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5)
