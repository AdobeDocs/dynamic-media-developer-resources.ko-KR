---
title: ZoomView.enableHD
description: ZoomView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: b3cc32ef-dd6c-47a3-9e55-86a43e874a84
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 3%

---

# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`숫자`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 항상|제한 안 함|제한</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> devicePixelRatio</span>이 <span class="codeph"> 1</span>보다 큰 장치의 최적화를 활성화하거나, 제한하거나, 비활성화합니다. iPhone4 및 이와 유사한 장치와 같이 고밀도 디스플레이를 사용하는 장치에 영향을 줍니다. 활성화된 경우 구성 요소는 장치의 픽셀 비율이 <span class="codeph"> 1</span>인 것처럼 IS 이미지 요청의 크기를 제한하여 대역폭을 줄입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 숫자</span></span> </p> </td> 
   <td colname="col2"> <p> 제한 설정을 사용하는 경우 구성 요소는 높은 픽셀 밀도를 지정된 제한까지만 활성화합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택적.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`limit,1500`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enableHD=always`
