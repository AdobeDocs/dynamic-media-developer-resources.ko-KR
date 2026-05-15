---
title: op_noise
description: 노이즈를 추가합니다. 전경 이미지 데이터나 효과 레이어의 전경에 임의의 노이즈를 추가합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eeadd3ab-80ff-4f9b-b5b7-4f3da6feebde
TQID: 'https://experienceleague.adobe.com/Awfk7mrYylvJeu8mSTa--aSoVMx8Mk6IqDC6ZtFFu4U'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 92
ht-degree: 1%

---

# op_noise{#op-noise}

노이즈를 추가합니다. 전경 이미지 데이터나 효과 레이어의 전경에 임의의 노이즈를 추가합니다.

`op_noise= *`val`*[,uniform|gaussian[, *`흑백`*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 값</span> </p> </td> 
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

회색 음영 이미지에는 *`monochrome`*&#x200B;이(가) 무시됩니다.

## 속성 {#section-1f1a64c791f545a3bf1abd0b0e575d87}

레이어 명령. `layer=comp`인 경우 현재 레이어 또는 합성 이미지에 적용됩니다.

## 기본값 {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0`(노이즈 없음).
