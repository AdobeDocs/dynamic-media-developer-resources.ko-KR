---
title: res
description: 재질 해상도. 반복 가능한 텍스처 또는 데칼 이미지의 해상도를 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f207355d-5819-47fc-bda5-27a411449569
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 2%

---

# res{#res}

재질 해상도. 반복 가능한 텍스처 또는 데칼 이미지의 해상도를 지정합니다.

` res= *`val`*`

<table id="simpletable_2004B804D46E43C090E59BBFF8144598"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>해상도, 재료 해상도 단위(일반적으로 인치당 픽셀 수)(실수). </p> </td> 
 </tr> 
</table>

데칼소재가 있으면, `size=` 두 가지 모두 `size=` 및 `res=` 을(를) 지정합니다.

## 속성 {#section-6a458ddc202f46e0b668c9f040a65cef}

재질 속성입니다. 단색 소재에서 무시됨. 캐비닛과 창 커버링 재료로만 제작됩니다.

## 기본값 {#section-ee4088a994014df59105fc1dbb2aa042}

`catalog::Resolution`, 자료가 카탈로그 항목을 기반으로 하는 경우, 그렇지 않은 경우 `attribute::Resolution`, `res= is` 이(가) 지정되지 않았거나 0보다 작거나 같은 값으로 설정되었습니다.

## 참조 {#section-c00f6fb7b3e74719ac361de9a9ce4e52}

[재질 해상도](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b), [size=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988), [catalog::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-6a2d64c2d72b438fade58a3391569da7), [attribute::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
