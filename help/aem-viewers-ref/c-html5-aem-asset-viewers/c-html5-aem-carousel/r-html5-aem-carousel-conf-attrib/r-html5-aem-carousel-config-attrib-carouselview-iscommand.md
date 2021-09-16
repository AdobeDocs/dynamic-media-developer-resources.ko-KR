---
title: CarouselView.iscommand
description: CarouselView.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 848eaed7-c150-4537-96a4-f2614162d58f
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 10%

---

# CarouselView.iscommand{#carouselview-iscommand}

` [CarouselView.|<containerId>_carouselView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand  </span></span> </p> </td> 
   <td colname="col2"> <p> 배너 이미지에 적용되는 이미지 제공 명령 문자열입니다. URL에 지정된 경우 <span class="codeph"> &amp;</span> 및 <span class="codeph"> =</span>의 모든 항목은 각각 <span class="codeph"> %26</span> 및 <span class="codeph"> %3D</span>로 HTTP로 인코딩되어야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

없음.

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

뷰어 URL에 지정된 경우:

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

구성 데이터에 지정되는 경우:

`iscommand=op_sharpen=1&op_colorize=0xff0000`
