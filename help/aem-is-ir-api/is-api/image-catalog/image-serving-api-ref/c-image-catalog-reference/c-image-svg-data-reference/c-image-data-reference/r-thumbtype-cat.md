---
description: 축소판 유형. 이 이미지의 축소판을 생성하는 방법을 설명합니다.
seo-description: 축소판 유형. 이 이미지의 축소판을 생성하는 방법을 설명합니다.
seo-title: ThumbType
solution: Experience Manager
title: ThumbType
topic: Scene7 Image Serving - Image Rendering API
uuid: b737b5a4-ad6d-4a9c-b48f-81cf170dd210
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ThumbType{#thumbtype}

축소판 유형. 이 이미지의 축소판을 생성하는 방법을 설명합니다.

다음 축소판 유형이 지원됩니다.

<table id="simpletable_874E4190A1DC4FB0AE1B2E3734746527"> 
 <tr class="strow"> 
  <td class="stentry"> <p>자르기(1) </p></td> 
  <td class="stentry"> <p>이미지를 축소판 종횡비로 자릅니다. 축소판 사각형과 이미지의 종횡비가 정확히 동일하지 않은 경우 이미지의 일부가 잘려 전체 축소판 사각형이 이미지 데이터로 채워지도록 합니다. 자르기 사각형은 <span class="codeph"> 특성::ThumbHorizAlign 및</span> attribute::ThumbVertAlign을 사용하여 이미지에 위치합니다 <span class="codeph"></span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>맞춤(2) </p></td> 
  <td class="stentry"> <p>전체 이미지를 축소판 사각형에 맞춥니다. 이미지는 <span class="codeph"> :ThumbHorizAlign 및 특성:ThumbVertAlign을 사용하여 축소판 사각형</span> 내에 배치되며 <span class="codeph"> 추가 공간은</span>:ThumbBkgColor로 채워집니다 <span class="codeph"></span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>텍스처(3) </p></td> 
  <td class="stentry"> <p>해상도에 따라 이미지를 자릅니다. 이미지는 <span class="codeph"> 카탈로그:ThumbRes와 카탈로그:</span> :Resolution의 비율로 <span class="codeph"> 조정됩니다</span>. 결과 이미지가 축소판보다 크면 크기에 맞게 잘립니다. 크기 조절된 이미지가 축소판보다 작은 경우 나머지 영역은 <span class="codeph"> :ThumbBkgColor 속성으로 채워집니다</span>. <span class="codeph"> attribute::ThumbHorizAlign</span> 및 <span class="codeph"> attribute::ThumbVertAlign은</span> 큰 이미지 내의 자르기 사각형 위치나 축소판 내의 작은 이미지 위치를 결정하는 데 사용됩니다. </p></td> 
 </tr> 
</table>

클라이언트는 `req=tmb` 요청과 함께 이미지 축소판을 요청합니다.

## 속성 {#section-c58a8e67c2134ca3a0edd21b20dd3052}

열거형 값. 유효한 값은 1, 2 또는 3이며 각각 자르기, 맞추기 및 텍스처 유형에 해당합니다.

## 기본값 {#section-a6a7c43a83384a4aab861a48d73c7c26}

`attribute::ThumbType` 값이 0이거나 필드가 비어 있는 경우 필드가 없는 경우에 사용됩니다.

## 참조 {#section-fc1a79d3e6274b4381a17da159649a07}

[attribute::Type](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbtype.md#reference-329e9dbf3e5f49548d1eb61915b538f5) , [attribute::BkgColor](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbbkgcolor.md#reference-8e38088e79a54446a9106d0b93c9b31e), [attribute::ThumbThumb](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbhorizalign.md#reference-0ae8b88669df4769a9053b22aca33691), [attribute::ThumbAlign,](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbvertalign.md#reference-d47c6b34588c4855b04ad134e472f04f)특성 Vert, Catalog [](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69)[](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1)[](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)[Catalog:Res Align Res Price, CatalogResolution:ReliteMb Thumb, ThumbnailThumbThumb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
