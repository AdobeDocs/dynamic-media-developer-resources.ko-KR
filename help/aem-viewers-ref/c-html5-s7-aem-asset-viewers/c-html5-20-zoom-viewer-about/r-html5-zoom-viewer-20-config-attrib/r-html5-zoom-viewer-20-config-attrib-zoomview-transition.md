---
description: ZoomView.transition
solution: Experience Manager
title: ZoomView.transition
feature: Dynamic Media Classic,Viewers,SDK/API,확대/축소
role: Developer,Business Practitioner
exl-id: f1b4faa3-14d1-4eef-acc2-214c7be4a5ab
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 4%

---

# ZoomView.transition{#zoomview-transition}

` [ZoomView.|<containerId>_zoomView.]transition= *``*[, *`시간 제한`*]`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 시간</span></span> </p> </td> 
   <td colname="col2"> <p> 단일 확대/축소 단계 작업에 대한 애니메이션이 수행하는 시간(초)을 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 완화</span></span> </p> </td> 
   <td colname="col2"> <p> 전환이 보다 자연스러운 것처럼 보이게 하는 가속 또는 감속이라는 환상을 만듭니다. 완화를다음 중 하나로 설정할 수 있습니다. </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0(자동) </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1(선형) </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2(이차) </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3(세제곱근) </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4(사분위수) </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5(경단위) </li> 
     </ul> </p> <p>자동 모드는 탄력적 확대/축소가 비활성화된 경우 항상 선형 전환을 사용합니다(기본값). 그렇지 않으면 전환 시간을 기반으로 하는 다른 완화 기능 중 하나에 해당합니다. 즉, 전환 시간이 짧을수록 완화 기능이 향상되어 가속 또는 감속 효과를 가속화할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`0.5,0`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`transition=2,2`
