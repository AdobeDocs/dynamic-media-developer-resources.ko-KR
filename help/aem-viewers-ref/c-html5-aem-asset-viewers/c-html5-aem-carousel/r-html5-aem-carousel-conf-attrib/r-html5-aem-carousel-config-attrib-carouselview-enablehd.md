---
title: CarouselView.enableHD
description: CarouselView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: c94ac151-3115-42ac-8a76-13b8769293cb
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 3%

---

# CarouselView.enableHD{#carouselview-enablehd}

` [CarouselView.|<containerId>_carouselView.]enableHD=always|never|limit[, *`숫자`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 항상|제한 안 함|제한</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> devicePixelRatio</span>이 <span class="codeph"> 1</span>보다 큰 장치, 즉, iPhone4 및 이와 유사한 장치와 같이 고밀도 디스플레이를 사용하는 장치의 최적화를 활성화, 제한 또는 비활성화합니다. </p> <p>활성화하면 구성 요소가 장치의 픽셀 비율이 <span class="codeph"> 1</span>인 것처럼 IS 이미지 요청의 크기를 제한하여 대역폭을 줄입니다. </p> <p>아래 예를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 숫자</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 제한</span> 설정을 사용하는 경우 구성 요소는 높은 픽셀 밀도를 지정된 제한까지만 활성화합니다. </p> <p>아래 예를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택적.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`limit,1500`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enableHD=always`
