---
title: op_noise
description: 노이즈를 추가합니다. 전경 이미지 데이터나 효과 레이어의 전경에 임의의 노이즈를 추가합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eeadd3ab-80ff-4f9b-b5b7-4f3da6feebde
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 1%

---

# op_noise{#op-noise}

노이즈를 추가합니다. 전경 이미지 데이터나 효과 레이어의 전경에 임의의 노이즈를 추가합니다.

`op_noise= *`val`*[,uniform|gaussian[, *`단색`*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> val</span> </p> </td> 
   <td colname="col2"> <p>노이즈의 양(%)(0...100int). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 균일</span> </p> </td> 
   <td colname="col2"> <p>균일한 노이즈 분포를 선택하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 가우스</span> </p> </td> 
   <td colname="col2"> <p>가우시안 노이즈 분포를 선택합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 단색</span> </p> </td> 
   <td colname="col2"> <p>색상 노이즈의 경우 0으로, 회색 노이즈의 경우 1로 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`monochrome`* 회색 음영 이미지에는 무시됩니다.

## 속성 {#section-1f1a64c791f545a3bf1abd0b0e575d87}

레이어 명령. 다음과 같은 경우 현재 레이어 또는 합성 이미지에 적용됩니다. `layer=comp`.

## 기본값 {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0`, 노이즈 없음.
