---
description: FlyoutZoomView.flyouttransition
solution: Experience Manager
title: FlyoutZoomView.flyouttransition
uuid: f1a9f2bc-9a13-4980-9241-e835a0aadd2c
feature: Dynamic Media Classic,뷰어,SDK/API,플라이아웃
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---


# FlyoutZoomView.flyouttransition{#flyoutzoomview-flyouttransition}

` [FlyoutZoomView.|<containerId>_flyout.]flyouttransition=[none|slide|fade][, *``*[, *``*[, *``*[, *`showtimeshodelayhidetimehidedelay`*]]]]`

<table id="table_AB421835D2454ECD8AA40DBFADBAC65F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 없음|슬라이드|페이드  </span> </span> </p> </td> 
   <td colname="col2"> <p> 플라이아웃 보기를 표시하거나 숨길 때 적용되는 효과의 유형을 지정합니다. <span class="codeph"> 없음 </span>을 사용하면 플라이아웃 이미지가 활성화되고 준비되면 즉시 표시됩니다.<span class="codeph"> 슬라이드 </span>을 사용하면 슬라이드 애니메이션이 왼쪽에서 오른쪽으로 재생됩니다.<span class="codeph"> 페이드 </span>는 플라이아웃 이미지에 알파 전환을 적용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime  </span> </span> </p> </td> 
   <td colname="col2"> <p> 애니메이션 표시를 완료하는 데 걸리는 시간(초)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showdelay  </span> </span> </p> </td> 
   <td colname="col2"> <p> 애니메이션 표시를 시작하는 사용자 동작과 애니메이션 자체의 표시 시작 사이의 지연 시간(초)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hidetime  </span> </span> </p> </td> 
   <td colname="col2"> <p> 애니메이션 숨기기가 완료되는 데 걸리는 시간(초)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hidedelay  </span> </span> </p> </td> 
   <td colname="col2"> <p> 애니메이션 숨기기를 시작하는 사용자 동작 사이의 지연 시간(초)과 애니메이션 숨기기 자체의 시작 시간입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

선택 사항입니다.

## 기본값 {#section-a08032f0fcf041c09e63c0238a339fc9}

`fade,1,0,1,0`

## 예 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`flyouttransition=slide,1,1,2,1`
