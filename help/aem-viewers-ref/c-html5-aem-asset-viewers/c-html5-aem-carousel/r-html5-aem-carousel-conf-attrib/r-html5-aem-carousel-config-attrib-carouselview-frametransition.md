---
title: CarouselView.frametransition
description: CarouselView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 771395fb-775d-462e-86dc-0600cfecb345
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 6%

---

# CarouselView.frametransition{#carouselview-frametransition}

` [CarouselView.|<containerId>_carouselView.]frametransition=none|fade|slide[, *``*[, *`지속 시간 간격`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|페이드|슬라이드  </span> </p> </td> 
   <td colname="col2"> <p>프레임 변경에 적용되는 효과의 유형을 지정합니다. 예를 들어, <span class="codeph"> 어떤 </span>도 전환되지 않는 것을 의미합니다. 프레임 변경은 즉시 발생합니다. 및, </p> <p> <span class="codeph"> 페이드 </span> 는 이전 프레임과 새 프레임 간에 교차 페이드 전환을 의미합니다. 마지막으로 </p> <p> <span class="codeph"> 슬라이드 </span> 가 이전 프레임이 보기에서 슬라이딩되고 새 프레임이 슬라이딩되는 전환을 활성화합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 기간  </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 페이드 </span> 또는 <span class="codeph"> 슬라이드 </span> 전환 효과의 기간(초)을 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 간격  </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 슬라이드 </span> 전환에서 인접한 프레임 사이의 간격은 <span class="codeph"> 0 </span>부터 <span class="codeph"> 1까지의 범위를 가지며, 구성 요소의 너비를 기준으로 합니다.</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

없음.

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,0.3`
