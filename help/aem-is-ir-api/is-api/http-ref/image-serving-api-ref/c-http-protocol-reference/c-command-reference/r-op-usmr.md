---
description: 언샵 마스크 [언샵]을 사용하면 레이어=comp인 경우 모든 크기 조절 후에 레이어 또는 최종 보기 이미지가 마스크됩니다.
solution: Experience Manager
title: op_usmR
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 51a779be-568b-40e5-99d9-e875023a2b2c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 3%

---

# op_usmR{#op-usmr}

언샵 마스크 [언샵]을 사용하면 레이어=comp인 경우 모든 크기 조절 후에 레이어 또는 최종 보기 이미지가 마스크됩니다.

매개 변수는 다운 샘플링이 발생했는지 여부에 관계없이 그대로 적용됩니다.

`op_usmR= *`금액`*[, *`radiusR`*[, *`임계값`*[, *`단색`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 금액</span></span> </p></td> 
  <td class="stentry"> <p>필터 강도 요소(실수 0...5). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p></td> 
  <td class="stentry"> <p>픽셀 단위의 필터 커널 반경(실수 0...250). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 임계값</span></span> </p></td> 
  <td class="stentry"> <p>필터 임계값 수준(int 0...255). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 단색</span></span> </p></td> 
  <td class="stentry"> <p>각 색상 구성 요소에 별도로 적용하려면 0을 이미지 밝기(강도)에만 적용하려면 1을 설정합니다. </p> <p><span class="codeph"> <span class="varname"> 단색</span></span> 회색 음영 이미지에는 무시됩니다. </p> </td> 
 </tr> 
</table>

레이어 마스크 또는 복합 마스크도 선명하게 됩니다.

## 속성 {#section-fb5311b34d164946b74dadb32359518a}

Layer 속성 또는 view 속성. 다음과 같은 경우 현재 레이어 또는 최종 뷰 이미지에 적용됩니다. `layer=comp`. 효과 레이어는 이를 무시합니다.

## 기본값 {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usmR=0,0,0,0` 언샵 마스킹 효과 없음.

## 참조 {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) , [op_usm](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa)
