---
description: 이미지를 확대/축소합니다. 형태 확장(반경 > 0) 또는 손상(반경 < 0)을 마스크 데이터에 적용합니다.
seo-description: 이미지를 확대/축소합니다. 형태 확장(반경 > 0) 또는 손상(반경 < 0)을 마스크 데이터에 적용합니다.
seo-title: op_growMaskR
solution: Experience Manager
title: op_growMaskR
topic: Scene7 Image Serving - Image Rendering API
uuid: b81968e7-ebaf-426c-9230-1afcf4b5cf24
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_growMaskR{#op-growmaskr}

이미지를 확대/축소합니다. 형태 확장(반경 > 0) 또는 손상(반경 &lt; 0)을 마스크 데이터에 적용합니다.

`op_growMaskR= *`radiusR`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p> </td> 
  <td class="stentry"> <p>마스크가 다운샘플링되었는지 여부에 관계없이 반경 R <span class="codeph"><span class="varname"> 이</span></span> 적용되는 반경(픽셀 단위: -100.100)을 그대로 늘리거나 감소시킵니다. </p></td> 
 </tr> 
</table>

마스크의 가장자리 주위의 결함을 방지하기 위해 마스크를 약간 확대하거나 축소하는 데 주로 사용됩니다.

## 속성 {#section-b1c66d65168d4ea695e8662ea690bd4e}

현재 레이어나 `0` 해당하는 경우 레이어에 적용됩니다 `layer=comp`.

## 기본값 {#section-14c908bb87cb42acbea709effea2f964}

`op_growMaskR=0`을 클릭합니다.

## 참조 {#section-ad3e5cecfc3448a38ea06093e015c88a}

[레이어 효과](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_grow](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_growMask](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmask.md#reference-f0f9000af3ae43aba73d3ac1826710a1)
