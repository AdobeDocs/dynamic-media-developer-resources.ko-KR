---
description: 널
seo-description: 널
seo-title: ZoomView.transition
solution: Experience Manager
title: ZoomView.transition
topic: Dynamic media
uuid: f579397b-a449-42fe-b0a7-f0da65a6a248
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.transition{#zoomview-transition}

` [ZoomView.|<containerId>_zoomView.]transition= *``*[, *`시간 절약`*]`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 시간</span></span> </p> </td> 
   <td colname="col2"> <p> 단일 확대/축소 단계 동작에 대해 애니메이션이 수행하는 시간(초)을 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 속도</span></span> </p> </td> 
   <td colname="col2"> <p> 가속도 또는 감속 효과를 만들어 전환이 보다 자연스럽게 표시되도록 합니다. 다음 중 하나로 부드럽게를 설정할 수 있습니다. </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0(자동) </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1(선형) </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2(이차) </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3(세제곱인치) </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4(사분위수) </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5. (퀴틱) </li> 
     </ul> </p> <p>자동 모드는 탄력적인 확대/축소가 비활성화된 경우 항상 선형 전환을 사용합니다(기본값). 그렇지 않으면 전환 시간을 기반으로 하는 다른 여유 함수 중 하나에 해당합니다. 즉, 전환 시간이 짧을수록 가속 또는 감속 효과를 가속화하는 데 속도 기능이 더 많이 사용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-50bcd15223174bb79ce08b31ea03d682}

선택 사항입니다.

## 기본값 {#section-7564169749ff4a4996049ea1148cb2a5}

`0.5,0`

## 예 {#section-96e69b70365f461dae4399e49044ea2f}

`transition=2,2`
