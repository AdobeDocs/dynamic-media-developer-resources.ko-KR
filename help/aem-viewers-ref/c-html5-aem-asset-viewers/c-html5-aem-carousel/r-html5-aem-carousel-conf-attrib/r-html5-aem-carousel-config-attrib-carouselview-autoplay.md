---
description: 회전판 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
title: CarouselView.autoplay
feature: Dynamic Media Classic,뷰어,SDK/API,회전판 배너
role: 개발자,비즈니스 전문가
exl-id: 43b5c169-0ef6-4a12-a777-d36c1a8d1771
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 5%

---

# CarouselView.autoplay{#carouselview-autoplay}

회전판 뷰어에 대한 구성 속성입니다.

`[CarouselView.|<containerId>_carouselView.]autoplay=[0|1][,duration][,direction]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">[0|1][,지속 시간][,방향]</span> </p> </td> 
   <td colname="col2"> <p> 회전 메뉴에 각 배너를 표시할 시작/해제 시간 및 자동 루프 방향을 지정합니다. </p> <p>자동 루프를 해제하려면 <span class="codeph"> 0</span>으로 설정합니다. </p> <p><span class="codeph"> 1</span>을(를) 전환 지속 시간이 <span class="codeph"> 기간</span>에 의해 제어되는 자동 루프되도록 설정합니다. </p> <p>자동 루프 방향은 <span class="codeph"> 방향</span>으로 제어됩니다. <span class="codeph"> 방향</span>의 범위는 <span class="codeph"> 1</span> 오른쪽에서 왼쪽으로 <span class="codeph"> 0</span> 왼쪽에서 오른쪽 사이의 범위입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`1,9`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
autoplay=1,2,1
```
