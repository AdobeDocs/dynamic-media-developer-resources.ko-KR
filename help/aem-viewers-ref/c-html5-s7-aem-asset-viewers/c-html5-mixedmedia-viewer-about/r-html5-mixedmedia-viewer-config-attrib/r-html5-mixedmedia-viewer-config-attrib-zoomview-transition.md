---
title: ZoomView.transition
description: ZoomView.transition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: bb00a1c9-aa6f-428f-8d57-241ee1efa082
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 2%

---

# ZoomView.transition{#zoomview-transition}

` [ZoomView.|<containerId>_zoomView.]transition= *`시간`*[, *`완화`*]`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 시간</span></span> </p> </td> 
   <td colname="col2"> <p> 단일 확대/축소 단계 작업의 애니메이션에 걸리는 시간을 초 단위로 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 완화</span></span> </p> </td> 
   <td colname="col2"> <p> 가속 또는 감속 효과를 만들어 전환이 자연스럽게 보이도록 합니다. 완화를 다음 중 하나로 설정할 수 있습니다. </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0(자동) </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1(선형) </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2(2차) </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3(3차) </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4(4차) </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5(5차) </li> 
     </ul> </p> <p>자동 모드에서는 탄력적인 확대/축소가 비활성화되어 있으면(기본값) 항상 선형 전환을 사용합니다. 그렇지 않으면 전환 시간을 기준으로 다른 완화 기능 중 하나에 맞습니다. 즉, 전이 시간이 짧을수록 더 높은 완화 함수를 사용하여 가속 또는 감속 효과를 가속화시킨다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택적.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0.5,0`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=2,2`
