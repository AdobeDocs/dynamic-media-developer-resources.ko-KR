---
description: SpinView.transition
solution: Experience Manager
title: SpinView.transition
feature: Dynamic Media Classic,Viewers,SDK/API,혼합 미디어 집합
role: Developer,User
exl-id: fcffe282-65a5-4093-8838-71a64085b387
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 4%

---

# SpinView.transition{#spinview-transition}

` [SpinView.|<containerId>_spinView.]transition= *``*[, *`시간 제한`*]`

<table id="table_5B8094216AE94DC59671E06DB941A366"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 시간</span></span> </p> </td> 
   <td colname="col2"> <p> 단일 확대/축소 단계 작업에 대한 애니메이션이 수행하는 시간(초)을 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 완화</span></span> </p> </td> 
   <td colname="col2"> <p> 전환이 보다 자연스러운 것처럼 보이게 하는 가속 또는 감속이라는 환상을 만듭니다. 완화를다음 중 하나로 설정할 수 있습니다. </p> <p> 
     <ul id="ul_7B9694978D96449AB986AED1CF7F649D"> 
      <li id="li_904CEC8AD5834139A5585EE70ACE9C80">0(자동) </li> 
      <li id="li_471D4CD39C10415497B1714B0AD961B9"> 1(선형) </li> 
      <li id="li_7A0F9F1186604E75BAA19626A844236A"> 2(이차) </li> 
      <li id="li_B8D4C40D795642AB835925582B707158"> 3(세제곱근) </li> 
      <li id="li_2B9F7324BB89455C89C1CAE1BD5BBB65"> 4(사분위수) </li> 
      <li id="li_B94A553B6E844247BE88ECA0A8CEB811"> 5(경단위) </li> 
     </ul> </p> <p>자동 모드는 탄력적 확대/축소가 비활성화된 경우 항상 선형 전환을 사용합니다(기본값). 그렇지 않으면 전환 시간을 기반으로 하는 다른 완화 기능 중 하나에 해당합니다. 즉, 전환 시간이 짧을수록 완화 기능이 향상되어 가속 또는 감속 효과를 가속화할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0.5,0`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=2,2`
