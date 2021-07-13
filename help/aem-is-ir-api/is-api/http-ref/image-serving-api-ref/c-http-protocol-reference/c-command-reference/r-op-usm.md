---
description: 언샵 마스크 [언샵]을 선택하면 레이어 또는 최종 보기 이미지가 모든 크기 조절 후 레이어=comp인 경우 마스크됩니다.
solution: Experience Manager
title: op_usm
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a83d6326-9029-4c5c-a069-92bc81120866
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 6%

---

# op_usm{#op-usm}

언샵 마스크 [언샵]을 선택하면 레이어 또는 최종 보기 이미지가 모든 크기 조절 후 레이어=comp인 경우 마스크됩니다.

매개 변수는 전체 해상도 이미지에 적용되는 것으로 간주되며 다운샘플링된 이미지를 처리할 때 크기가 줄어듭니다.

`op_usm= *``*[, *``*[, *``*[, *`amountradituthroudmonochrome`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 금액</span></span> </p></td> 
  <td class="stentry"> <p>필터 강도 계수(실수 0...5). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 반경</span></span> </p></td> 
  <td class="stentry"> <p>커널 반경을 픽셀 단위로 필터링(실수 0...250). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 임계값</span></span> </p></td> 
  <td class="stentry"> <p>필터 임계값 수준(int 0...255). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 단색</span></span> </p></td> 
  <td class="stentry"> <p>각 색상 구성 요소에 개별적으로 적용하려면 0으로 설정하고, 이미지 밝기(강도)에만 적용하려면 1로 설정하십시오. </p> <p> <span class="codeph"><span class="varname"> </span></span> 회색 음영 이미지에 대해서는 모노크로메인이 무시됩니다. </p></td> 
 </tr> 
</table>

레이어 마스크나 복합 마스크도 선명하게 표시됩니다.

## 속성 {#section-fb5311b34d164946b74dadb32359518a}

레이어 특성 또는 보기 속성입니다. `layer=comp`인 경우 현재 레이어 또는 최종 보기 이미지에 적용됩니다. 효과 레이어에서 무시됨.

## 기본값 {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usm=0,0,0,0` - 언샵 마스킹 효과 없음

## 참조 {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [op_선명하게=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) ,  [op_usmR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usmr.md#reference-c0168bc1e3a24370883670c09bcb0fef)
