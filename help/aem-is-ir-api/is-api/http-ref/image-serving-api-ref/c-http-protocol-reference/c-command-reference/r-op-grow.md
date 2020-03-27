---
description: 이미지를 확대/축소합니다. 형태적 팽창을 적용하거나(반경 > 0) 누름(반경 < 0))을 이미지 데이터에 적용합니다.
seo-description: 이미지를 확대/축소합니다. 형태적 팽창을 적용하거나(반경 > 0) 누름(반경 < 0))을 이미지 데이터에 적용합니다.
seo-title: op_grow
solution: Experience Manager
title: op_grow
topic: Scene7 Image Serving - Image Rendering API
uuid: bc9bf889-f7e1-4a65-b6d6-7e1257ef8c11
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_grow{#op-grow}

이미지를 확대/축소합니다. 형태적 팽창을 적용하거나(반경 > 0) 누름(반경 &lt; 0))을 이미지 데이터에 적용합니다.

`op_grow= *`반경`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 반경</span></span> </p> </td> 
  <td class="stentry"> <p>반경을 픽셀 단위(int -100.100)로 확대/축소합니다. </p></td> 
 </tr> 
</table>

` *`반경은`*` 합성 이미지를 기준으로 픽셀 단위입니다. 이미지가 색상이면 각 구성 요소는 독립적으로 처리됩니다.

주로 레이어 효과의 크기를 수정하는 데 사용됩니다. 또한 마스크가 있는 텍스트 레이어 또는 단색 레이어에 특수 효과를 적용하는 데 유용합니다.

## 속성 {#section-b1c66d65168d4ea695e8662ea690bd4e}

레이어 특성. 현재 레이어 또는 합성 이미지에 적용됩니다( `layer=comp`경우).

## 기본값 {#section-14c908bb87cb42acbea709effea2f964}

`op_grow=0`을 클릭합니다.

## 참조 {#section-ad3e5cecfc3448a38ea06093e015c88a}

[레이어 효과](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)
