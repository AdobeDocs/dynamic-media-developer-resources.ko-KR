---
title: CarouselView.iscommand
description: CarouselView.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 848eaed7-c150-4537-96a4-f2614162d58f
TQID: 'https://experienceleague.adobe.com/L9gZx2DGIv6gDtuvwc5Q5-4PxH-K4oqw34qJH3kRrow'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 52
ht-degree: 7%

---

# CarouselView.iscommand{#carouselview-iscommand}

` [CarouselView.|<containerId>_carouselView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand </span></span> </p> </td> 
   <td colname="col2"> <p> 배너 이미지에 적용되는 이미지 제공 명령 문자열. URL에 지정되는 경우 <span class="codeph"> &amp;</span> 및 <span class="codeph"> =</span>은(는) 각각 <span class="codeph"> %26</span> 및 <span class="codeph"> %3D</span>(으)로 HTTP 인코딩이 적용되어야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택적.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

없음.

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

뷰어 URL에 지정되는 경우:

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

구성 데이터에 지정된 경우:

`iscommand=op_sharpen=1&op_colorize=0xff0000`
