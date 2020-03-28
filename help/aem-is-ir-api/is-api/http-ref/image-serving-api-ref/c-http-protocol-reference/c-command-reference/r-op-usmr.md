---
description: 언샵 마스크 레이어=comp인 경우, Unsharp는 모든 비율 조정 후 레이어 또는 최종 보기 이미지를 마스크합니다.
seo-description: 언샵 마스크 레이어=comp인 경우, Unsharp는 모든 비율 조정 후 레이어 또는 최종 보기 이미지를 마스크합니다.
seo-title: op_usmR
solution: Experience Manager
title: op_usmR
topic: Scene7 Image Serving - Image Rendering API
uuid: 98afd83c-097e-40b4-b0a6-647f70b95fae
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_usmR{#op-usmr}

언샵 마스크 레이어=comp인 경우, Unsharp는 모든 비율 조정 후 레이어 또는 최종 보기 이미지를 마스크합니다.

다운샘플링 발생 여부에 관계없이 매개 변수가 그대로 적용됩니다.

`op_usmR= *`Amountraditus`*[, *``*[, *``*[, *`Rthricoldmonochrome`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 금액</span></span> </p></td> 
  <td class="stentry"> <p>필터 강도 인수(실제 0...5). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p></td> 
  <td class="stentry"> <p>커널 반경(픽셀 단위: 실수 0...250) 필터링 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 임계값</span></span> </p></td> 
  <td class="stentry"> <p>필터 임계값 수준(int 0...255). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 단색</span></span> </p></td> 
  <td class="stentry"> <p>각 색상 구성 요소에 개별적으로 적용하려면 0으로, 이미지 밝기(강도)에만 적용하려면 1로 설정합니다. </p> <p><span class="codeph"> 회색 <span class="varname"> 음영</span></span> 이미지에는 모노크롬이 무시됩니다. </p> </td> 
 </tr> 
</table>

레이어 마스크 또는 합성 마스크도 선명하게 됩니다.

## 속성 {#section-fb5311b34d164946b74dadb32359518a}

레이어 특성 또는 보기 속성입니다. 현재 레이어 또는 최종 보기 이미지에 적용됩니다( `layer=comp`경우). 효과 레이어는 이를 무시합니다.

## 기본값 {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usmR=0,0,0,0` - 언샵 마스킹 효과 없음

## 참조 {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) , [op_usm](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa)
