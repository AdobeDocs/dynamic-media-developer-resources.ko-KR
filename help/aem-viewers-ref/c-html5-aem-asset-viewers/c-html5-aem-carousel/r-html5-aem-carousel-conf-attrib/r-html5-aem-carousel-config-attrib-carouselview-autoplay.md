---
title: CarouselView.autoplay
description: 슬라이드 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 43b5c169-0ef6-4a12-a777-d36c1a8d1771
TQID: 'https://experienceleague.adobe.com/LEeJUVIHLhplymrvp9IdNUWcfJz-Tl0kLffkik1GvkY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 81
ht-degree: 3%

---

# CarouselView.autoplay{#carouselview-autoplay}

슬라이드 뷰어에 대한 구성 속성입니다.

`[CarouselView.|<containerId>_carouselView.]autoplay=[0|1][,duration][,direction]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">[0|1][,duration][,direction]</span> </p> </td> 
   <td colname="col2"> <p> 설정/해제, 각 배너를 회전 메뉴에 표시하는 기간 및 자동 루프 방향을 지정합니다. </p> <p>자동 루프 끄기를 위해 <span class="codeph"> 0</span>(으)로 설정합니다. </p> <p>전환 기간이 <span class="codeph"> duration</span>에 의해 초 단위로 제어되도록 <span class="codeph"> 1</span>을(를) 자동 루프 설정으로 설정합니다. </p> <p>자동 루프의 방향이 <span class="codeph"> 방향</span>(으)로 제어됩니다. <span class="codeph"> 방향</span>의 범위는 <span class="codeph"> 1</span> 오른쪽에서 왼쪽으로 및 <span class="codeph"> 0</span> 왼쪽에서 오른쪽입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택적.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`1,9`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
autoplay=1,2,1
```
