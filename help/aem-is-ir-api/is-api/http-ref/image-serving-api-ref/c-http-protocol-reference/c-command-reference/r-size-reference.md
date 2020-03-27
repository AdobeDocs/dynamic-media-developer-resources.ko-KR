---
description: 레이어 크기 레이어에 회전=, 원근= 및 확장=이 적용되기 전에 레이어의 크기 또는 최대 레이어 크기를 지정합니다.
seo-description: 레이어 크기 레이어에 회전=, 원근= 및 확장=이 적용되기 전에 레이어의 크기 또는 최대 레이어 크기를 지정합니다.
seo-title: 크기
solution: Experience Manager
title: 크기
topic: Scene7 Image Serving - Image Rendering API
uuid: c9c13062-7974-4dd9-aff4-f9502bcf442e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 크기{#size}

레이어 크기 레이어에 회전=, 원근= 및 확장=이 적용되기 전에 레이어의 크기 또는 최대 레이어 크기를 지정합니다.

` size= *``*, *`위젯 높이`*`

` sizeN= *``*, *`widthNheightN`*`

<table id="simpletable_FBE17D736F93485AA0053BF447B4CC9F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 너비 <span class="varname"> , </span>높이 <span class="varname"> </span></span> </p> </td> 
  <td class="stentry"> <p>레이어 크기 제한(픽셀 단위, int, 0 이상)입니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 너비 <span class="varname"> N </span>, <span class="varname"> 높이N </span></span> </p> </td> 
  <td class="stentry"> <p>레이어 0 크기를 기준으로 표준화된 레이어 크기 제한(실제, 실제, 0.0...1.0) </p> </td> 
 </tr> 
</table>

이미지 레이어에 대해 지정할 때 size=는 레이어 이미지의 폭, 높이 또는 두 가지 모두를 제한합니다. 이미지 크기가 다음보다 크지 않도록 조정됩니다 `size=`. 정규화된 크기를 지정하면 레이어 0의 크기를 기준으로 합니다. 둘 다 *`width`* 및 *`height`* `crop=` 지정된 경우 소스 이미지의 크기가 조절되어(적용된 후) 둘 다 지정된 크기를 초과하지 않도록 합니다. 소스 사각형의 종횡비는 모든 경우에 그대로 유지됩니다. 또는 0으로 *`width`* 설정될 *`height`* 수 있습니다.이 경우 이 값은 서버의 이미지 종횡비를 기준으로 계산됩니다.

텍스트 레이어에 대해 지정할 때 텍스트 상자 크기를 `size=` 지정합니다. *`width`* 필수;0으로 *`height`* 설정할 수 있습니다. 이 경우 레이아웃된 텍스트의 높이가 레이어 높이로 사용됩니다. 기본적으로 텍스트 레이아웃 엔진은 텍스트 줄바꿈을 삽입하여 텍스트가 항상 사용 가능한 공간에 가로로 들어가도록 합니다. 을 *`height`* 지정하면 사용 가능한 공간에 맞지 않는 줄이 잘리거나 생략됩니다( `text=``textPs=`). `text=` 추가 맞춤 모드 지원자세한 내용은 을 `textAttr=` 참조하십시오.

단색 레이어에 대해 지정하면 정확한 레이어 크기를 `size=` 정의합니다.마스크를 제공하지 않는 한 두 값을 모두 지정해야 합니다. 또한 `mask=` 이 지정되어 있으면 이미지 레이어에서 이미지 크기가 조정되는 `size=` 것과 동일한 방식으로 마스크 이미지 크기가 지정됩니다.

## 속성 {#section-5f254b66fcba49bcb63f9c9ea40b230c}

레이어 특성. 해당되는 경우 레이어 0에 `layer=comp`적용됩니다. `sizeN=` 은 `layer=0` 또는 에 대해 허용되지 않습니다 `layer=comp`. `sizeN=` 은 워터마크 이미지를 정의하는 카탈로그 레코드에 `layer=0` `layer=comp` 대해서만 허용됩니다. 이 경우 `sizeN` 워터마크가 적용되는 합성 이미지를 기준으로 워터마크 이미지의 크기를 정의합니다. 이 `size=` 지정된 경우 이 레이어에 대해 `res=` 무시되고 `scale=` 무시됩니다. 효과 레이어에서 무시됩니다.

## 기본값 {#section-43d129deba6a441da66a1fdb63d1c85c}

`size=0,0`로 설정되어 있으면 레이어 크기가 제한되지 않습니다. 이미지 레이어의 경우 레이어 크기는 레이어 이미지 크기에 따라 `crop=`또는 작업이 적용된 후 `scale=`결정됩니다 `res=` . 텍스트 레이어의 경우 `size=` 지정하지 않으면 레이어 크기가 렌더링된 텍스트에 맞게 자동으로 조정됩니다.

단색 레이어에는 완전히 지정된 `size=`색상, `mask=`또는 `clipPath=`가 필요합니다.

## 예 {#section-d1adaddd9e0b4ca881fd8e0a7541e5d9}

템플릿의 [예](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) 를 [참조하십시오](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## 참조 {#section-63dfdf3750e249d2ab4c825ccd2e7181}

[scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065) , [res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)[, ClipPath=Following, Text Layers](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
