---
title: CarouselView.maxloadradius
description: CarouselView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 8a3d3d32-7970-420c-8ad8-296c9ba1f08a
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 6%

---

# CarouselView.maxloadradius{#carouselview-maxloadradius}

` [CarouselView.|<containerId>_carouselView.]maxloadradius=-1|0| *`preloadbr`*`

<table id="table_B3B03B00DCF0466DB332E851F4DDF610"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td> <p>구성 요소 사전 로드 동작을 지정합니다. </p> <p><span class="codeph"> -1</span> 로 설정하면 유휴 상태이면 구성 요소가 모든 캐러셀 프레임을 미리 로드합니다. </p> <p><span class="codeph"> 0</span> 로 설정하면 구성 요소는 현재 표시된 프레임, 이전 프레임 및 다음 프레임만 로드합니다. </p> <p><span class="codeph"><span class="varname"> </span></span>preloadnbrandroid는 유휴 상태에 있을 때 현재 표시된 프레임 주위에 표시되는 보이지 않는 프레임의 수를 정의합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`1`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`maxloadradius=0`
