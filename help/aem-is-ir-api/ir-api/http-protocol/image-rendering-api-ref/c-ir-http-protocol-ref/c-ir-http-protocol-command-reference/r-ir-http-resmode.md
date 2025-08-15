---
title: resMode
description: 재샘플링 모드. 렌더링된 이미지의 크기를 wid=, hei= 또는 scl=로 지정된 크기로 조정하는 데 사용할 리샘플링 및/또는 보간 알고리즘을 선택합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0926dcfe-881c-4b52-b08d-c56afa0ba04d
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 7%

---

# resMode{#resmode}

재샘플링 모드. 렌더링된 이미지를 `wid=`, `hei=` 또는 `scl=`(으)로 지정된 크기로 조정하는 데 사용할 재샘플링 및/또는 보간 알고리즘을 선택합니다.

` `resMode=bilin|bicub|sharp2|bisharp&quot;

<table id="table_AF954C101B30473FAFE9930C7B694305"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> 청구됨 </span> </p> </td> 
   <td colname="col2"> <p>표준 이중 선형 보간을 선택합니다. 가장 빠른 재샘플링 방법입니다. 일부 앨리어싱 가공물이 발생할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bicub </span> </p> </td> 
   <td colname="col2"> <p>쌍입방 보간을 선택합니다. 이중 선형 보간보다 CPU 집약적이나 덜 눈에 띄는 앨리어싱 아티팩트가 있는 더 선명한 이미지를 만듭니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> sharp2 </span> </p> </td> 
   <td colname="col2"> <p>보간 알고리즘으로 수정된 Lanczos Window 함수를 선택합니다. 높은 CPU 비용으로 bicubic보다 약간 더 선명한 결과를 낼 수 있습니다. </p> <p> <span class="codeph"> 선명하게 </span>이(가) <span class="codeph"> 선명하게2 </span>(으)로 바뀌었습니다. 이 경우 모아레라고도 하는 앨리어싱 아티팩트가 발생할 가능성이 낮습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bisharp </span> </p> </td> 
   <td colname="col2"> <p><span class="keyword"> Adobe Photoshop </span>에서 "bicubic sharper"라고 하는 이미지 크기를 줄이기 위해 <span class="keyword"> Adobe Photoshop </span> 기본 리샘플러를 선택합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-ea7029f37e094d9cb85646b85fbac0ce}

요청 내의 어느 곳에서든 발생할 수 있습니다. 최종 이미지 크기 조정이 적용되지 않으면 무시됩니다.

## 기본값 {#section-900872fb93dc41efb3e8ad5b62aadc38}

`attribute::ResMode`

## 참조 {#section-16c557a2250e4f04b3e6cbef18add9ce}

[특성::ResMode](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-resmode.md#reference-fdca7eb6d5104fdeae9d6ac42251db82) , [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)
