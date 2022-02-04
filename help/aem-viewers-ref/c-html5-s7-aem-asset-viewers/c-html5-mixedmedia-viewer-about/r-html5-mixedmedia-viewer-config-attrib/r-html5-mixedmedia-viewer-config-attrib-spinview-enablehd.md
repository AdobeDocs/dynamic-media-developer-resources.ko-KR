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
ht-degree: 7%

---

# SpinView.enableHD{#spinview-enablehd}

` [SpinView.|<containerId>_spinView.]enableHD=always|never|limit[, *`수`*]`

<table id="table_8929B59833DE4E1C89FA4BCF07309809"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 항상|절대 안 함|제한</span> </p> </td> 
   <td colname="col2"> <p> 다음의 장치에 대한 최적화를 활성화, 제한 또는 비활성화합니다. <span class="codeph"> devicePixelRatio</span> 보다 큼 <span class="codeph"> 1</span>: iPhone4 및 유사한 장치와 같은 고밀도 디스플레이를 사용하는 장치입니다. 활성 상태인 경우, 구성 요소는 IS 이미지 요청의 크기를 장치에 픽셀 비율만 있는 것처럼 제한합니다 <span class="codeph"> 1</span> 따라서 대역폭을 줄입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 수</span></span> </p> </td> 
   <td colname="col2"> <p> 를 사용하는 경우 <span class="codeph"> 제한</span> 이 설정을 사용하면 지정된 제한까지만 높은 픽셀 밀도를 사용할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`limit,1500`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`enableHD=always`
