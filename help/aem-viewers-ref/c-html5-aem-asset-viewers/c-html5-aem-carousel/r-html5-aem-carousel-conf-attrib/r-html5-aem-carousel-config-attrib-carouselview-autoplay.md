---
description: 회전판 뷰어에 대한 구성 속성입니다.
seo-description: 회전판 뷰어에 대한 구성 속성입니다.
seo-title: CarouselView.autoplay
solution: Experience Manager
title: CarouselView.autoplay
topic: Dynamic media
uuid: 12730b17-110e-405b-97fe-e70fab89c703
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# CarouselView.autoplay{#carouselview-autoplay}

회전판 뷰어에 대한 구성 속성입니다.

`[CarouselView.|<containerId>_carouselView.]autoplay=[0|1][,duration][,direction]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">[0|1][,지속 시간][,방향]</span> </p> </td> 
   <td colname="col2"> <p> 회전 메뉴에 각 배너를 표시할 시간(설정/해제)과 자동 루프의 방향을 지정합니다. </p> <p>자동 루프가 꺼지려면 <span class="codeph"> 0으로</span> 설정합니다. </p> <p>전환 지속 시간(초)을 기준으로 <span class="codeph"> 자동 루프가 설정되도록</span> 1 <span class="codeph"> 을</span>설정할 수 있습니다. </p> <p>자동 루프의 방향은 <span class="codeph"> 방향으로</span>제어됩니다. 방향은 <span class="codeph"></span> 1 <span class="codeph"> 오른쪽에서 왼쪽으로,</span> 0 <span class="codeph"> 왼쪽에서 오른쪽으로</span> 지정할 수 있습니다. </p> </td> 
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

