---
description: 언샵 마스크 레이어=comp인 경우, Unsharp는 모든 비율 조정 후 레이어 또는 최종 보기 이미지를 마스크합니다.
seo-description: 언샵 마스크 레이어=comp인 경우, Unsharp는 모든 비율 조정 후 레이어 또는 최종 보기 이미지를 마스크합니다.
seo-title: op_usm
solution: Experience Manager
title: op_usm
topic: Scene7 Image Serving - Image Rendering API
uuid: c647e063-2405-489b-b14d-a70638ac8af7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_usm{#op-usm}

언샵 마스크 레이어=comp인 경우, Unsharp는 모든 비율 조정 후 레이어 또는 최종 보기 이미지를 마스크합니다.

매개 변수는 전체 해상도 이미지에 적용된다고 가정하고 다운샘플링된 이미지를 처리할 때 축소됩니다.

`op_usm= *``*[, *``*[, *``*[, *`아모우너트라디탈로모크롬`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 금액</span></span> </p></td> 
  <td class="stentry"> <p>필터 강도 인수(실제 0...5). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 반경</span></span> </p></td> 
  <td class="stentry"> <p>커널 반경(픽셀 단위: 실수 0...250) 필터링 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 임계값</span></span> </p></td> 
  <td class="stentry"> <p>필터 임계값 수준(int 0...255). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 단색</span></span> </p></td> 
  <td class="stentry"> <p>각 색상 구성 요소에 개별적으로 적용하려면 0으로, 이미지 밝기(강도)에만 적용하려면 1로 설정합니다. </p> <p> <span class="codeph"><span class="varname"> 흑백</span></span> 이미지는 회색 음영 이미지에 대해 무시됩니다. </p></td> 
 </tr> 
</table>

레이어 마스크 또는 합성 마스크도 선명하게 됩니다.

## 속성 {#section-fb5311b34d164946b74dadb32359518a}

레이어 특성 또는 보기 속성입니다. 현재 레이어 또는 최종 보기 이미지에 적용됩니다( `layer=comp`경우). 효과 레이어에서 무시됩니다.

## 기본값 {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usm=0,0,0,0` - 언샵 마스킹 효과 없음

## 참조 {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) , [op_usmR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usmr.md#reference-c0168bc1e3a24370883670c09bcb0fef)
