---
description: 널
seo-description: 널
seo-title: PageView.transition
solution: Experience Manager
title: PageView.transition
topic: Dynamic media
uuid: f84da456-ac02-4037-b1fd-7440823eb1ef
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 6%

---


# PageView.transition{#pageview-transition}

` [PageView.|<containerId>_pageView.]transition= *`시간 `*[, *`단축`*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 시간</span></span> </p> </td> 
   <td colname="col2"> <p> 단일 확대/축소 단계 동작에 대해 애니메이션이 수행하는 시간(초)을 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 여유</span></span> </p> </td> 
   <td colname="col2"> <p> 전환이 보다 자연스럽게 보이도록 가속 또는 감속이라는 환영을 만듭니다. 부드럽게 속성을 다음 중 하나로 설정할 수 있습니다. </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0(자동) </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1(선형) </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2(2차) </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3(세제곱인치) </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4(사분위수) </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5(5) </li> 
     </ul> </p> <p>자동 모드는 탄력적인 확대/축소가 비활성화된 경우 항상 선형 전환을 사용합니다(기본값). 그렇지 않으면 전환 시간을 기반으로 하는 다른 여유 함수 중 하나에 해당합니다. 즉, 전환 시간이 짧을수록 가속 또는 감속 효과를 가속화하는 데 여유 함수가 더 많이 사용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-ebfd9162c8504666bf0e4485bf3b1383}

선택 사항입니다.

## 기본값 {#section-9f91ce6567384ab691e4d4f8a7015455}

`0.5,0`

## 예 {#section-cb6b8793ee9946b8bf1cfddab8612db5}

`transition=2,2`
