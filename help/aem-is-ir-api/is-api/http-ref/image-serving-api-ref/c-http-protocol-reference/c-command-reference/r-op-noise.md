---
description: 노이즈를 추가합니다. 전경 이미지 데이터 또는 효과 레이어의 전경에 임의 노이즈를 추가합니다.
solution: Experience Manager
title: op_noise
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eeadd3ab-80ff-4f9b-b5b7-4f3da6feebde
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 2%

---

# op_noise{#op-noise}

노이즈를 추가합니다. 전경 이미지 데이터 또는 효과 레이어의 전경에 임의 노이즈를 추가합니다.

`op_noise= *``*[,uniform|gaussian[, *`valmonochrome`*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> val</span> </p> </td> 
   <td colname="col2"> <p>노이즈 크기(%...100 int). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 균일</span> </p> </td> 
   <td colname="col2"> <p>균일한 노이즈 분포를 선택합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 가우스</span> </p> </td> 
   <td colname="col2"> <p>가우스 노이즈 분포를 선택합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 단색</span> </p> </td> 
   <td colname="col2"> <p>색상 노이즈의 경우 0으로, 회색 노이즈의 경우 1로 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`monochrome`* 회색 음영 이미지에 대해서는 이 무시됩니다.

## 속성 {#section-1f1a64c791f545a3bf1abd0b0e575d87}

레이어 명령. `layer=comp` 인 경우 현재 레이어 또는 복합 이미지에 적용됩니다.

## 기본값 {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0`: 노이즈가 없습니다.
