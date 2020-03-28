---
description: 재질 해상도. 반복 가능한 텍스처 또는 디칼 이미지의 해상도를 지정합니다.
seo-description: 재질 해상도. 반복 가능한 텍스처 또는 디칼 이미지의 해상도를 지정합니다.
seo-title: res
solution: Experience Manager
title: res
topic: Scene7 Image Serving - Image Rendering API
uuid: ae755a92-ad06-4cf2-b627-0b8b14e385c3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# res{#res}

재질 해상도. 반복 가능한 텍스처 또는 디칼 이미지의 해상도를 지정합니다.

` res= *`val`*`

<table id="simpletable_2004B804D46E43C090E59BBFF8144598"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>해결 방법;재료 해상도 단위(일반적으로 인치당 픽셀 수)(실제). </p> </td> 
 </tr> 
</table>

십진수 자료의 경우 `size=` 와 를 모두 지정하면 `size=` 일반이 `res=` 적용됩니다.

## 속성 {#section-6a458ddc202f46e0b668c9f040a65cef}

재료 속성. 단색 재질로 무시됩니다. 텍스처를 사용하는 경우에만 캐비닛과 창 덮기 재료로만 가능합니다.

## 기본값 {#section-ee4088a994014df59105fc1dbb2aa042}

`catalog::Resolution`, if the material is based on a catalog entry, or if `attribute::Resolution``res= is` not specified or set to a value less or equal to 0

## 참조 {#section-c00f6fb7b3e74719ac361de9a9ce4e52}

[자재 해상도](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b), [크기=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988), [카탈로그::해상도](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-6a2d64c2d72b438fade58a3391569da7), [속성::해상도](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
