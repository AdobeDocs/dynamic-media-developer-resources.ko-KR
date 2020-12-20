---
description: 널
seo-description: 널
seo-title: CarouselView.enableHD
solution: Experience Manager
title: CarouselView.enableHD
topic: Dynamic media
uuid: 17df4a68-a251-427c-a3c4-1e0679e3f8f1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 8%

---


# CarouselView.enableHD{#carouselview-enablehd}

` [CarouselView.|<containerId>_carouselView.]enableHD=always|never|limit[, *`수`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> iPhone4 및 이와 유사한 장치와 같은 고밀도 디스플레이가 있는 장치인 <span class="codeph"> devicePixelRatio</span>이(가) <span class="codeph"> 1</span>보다 큰 장치에 대한 최적화를 활성화, 제한 또는 비활성화합니다. </p> <p>활성 상태인 경우, 구성 요소는 마치 장치가 <span class="codeph"> 1</span>의 픽셀 비율만 있고 이렇게 하면 대역폭이 감소되는 것처럼 IS 이미지 요청의 크기를 제한합니다. </p> <p>아래 예를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 수</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 제한</span> 설정을 사용하는 경우 구성 요소는 지정된 제한까지 높은 픽셀 밀도를 활성화합니다. </p> <p>아래 예를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`limit,1500`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enableHD=always`
