---
description: 노이즈를 추가합니다. 전경 이미지 데이터 또는 효과 레이어의 전경에 임의의 노이즈를 추가합니다.
seo-description: 노이즈를 추가합니다. 전경 이미지 데이터 또는 효과 레이어의 전경에 임의의 노이즈를 추가합니다.
seo-title: op_noise
solution: Experience Manager
title: op_noise
topic: Scene7 Image Serving - Image Rendering API
uuid: 531f7a94-149b-4090-a163-a1895156250b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_noise{#op-noise}

노이즈를 추가합니다. 전경 이미지 데이터 또는 효과 레이어의 전경에 임의의 노이즈를 추가합니다.

`op_noise= *``*[,uniform|gaussian[, *`발모노크롬`*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> val</span> </p> </td> 
   <td colname="col2"> <p>노이즈 양(백분율)(0...100int). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 유니폼</span> </p> </td> 
   <td colname="col2"> <p>균일한 노이즈 분포를 선택합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 가우시안</span> </p> </td> 
   <td colname="col2"> <p>가우시안 노이즈 분포를 선택합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 단색</span> </p> </td> 
   <td colname="col2"> <p>색상 노이즈의 경우 0으로, 회색 노이즈의 경우 1로 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`monochrome`* 은 회색 음영 이미지에 대해 무시됩니다.

## 속성 {#section-1f1a64c791f545a3bf1abd0b0e575d87}

레이어 명령. 현재 레이어 또는 합성 이미지에 적용됩니다( `layer=comp`경우).

## 기본값 {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0`, no noise.
