---
title: SpinView.enableHD
description: SpinView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0a2abdc6-eae5-4dda-b749-599cd8a07a98
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 6%

---

# SpinView.enableHD{#spinview-enablehd}

` [SpinView.|<containerId>_spinView.]enableHD=always|never|limit[, *`수`*]`

<table id="table_8929B59833DE4E1C89FA4BCF07309809"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 항상|절대|제한</span> </p> </td> 
   <td colname="col2"> <p> 장치의 최적화를 활성화, 제한 또는 비활성화합니다. <span class="codeph"> devicePixelratio</span> 다음보다 큼 <span class="codeph"> 1</span>: iPhone 4 및 이와 유사한 장치와 같이 고밀도 디스플레이를 사용하는 장치입니다. 활성화하면 구성 요소는 장비의 픽셀 비율이 인 것처럼 IS 이미지 요청의 크기를 제한합니다. <span class="codeph"> 1</span> 따라서 대역폭이 감소합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 수</span></span> </p> </td> 
   <td colname="col2"> <p> 을 사용하는 경우 <span class="codeph"> 제한</span> 이 설정을 사용하면 구성 요소에서 지정된 제한까지만 높은 픽셀 밀도를 사용할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택적.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`limit,1500`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`enableHD=always`
