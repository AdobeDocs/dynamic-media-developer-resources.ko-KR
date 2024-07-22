---
title: FlyoutZoomView.zoomfactor
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 150968d2-aece-4d2a-b5a8-31b03dae25bb
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 1%

---

# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *`primaryFactor`*[,[ *`secondaryFactor`*][, *`upscale`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> 기본 보기를 기준으로 플라이아웃 보기의 이미지 확대율을 지정합니다. 정수 또는 부동 소수점 값 <span class="codeph"> 1.0</span> 이상이어야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> 강조 표시가 활성 상태일 때 기본 보기를 클릭하거나 탭하여 액세스할 수 있는 선택적 보조 요소를 지정할 수 있습니다. 두 번째 시간을 클릭하거나 탭하면 기본 확대/축소 요소로 되돌아갑니다. <span class="codeph"> -1</span> 값은 보조 확대/축소 비율을 사용하지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 업스케일</span></span> </p> </td> 
   <td colname="col2"> <p>구성 요소가 작은 이미지를 처리하는 방법을 지정합니다. </p> <p><span class="codeph"> 1</span>(으)로 설정하면 구성 요소가 기본 보기에 맞도록 기본 이미지를 상향 조정합니다. 또한 구성된 플라이아웃 창 영역을 완전히 채우도록 확대/축소 이미지를 업스케일합니다. </p> <p><span class="codeph"> 0</span>(으)로 설정하면 작은 이미지가 원래 해상도로 표시되고 기본 보기 영역과 플라이아웃 창 내부에 가운데에 표시됩니다. 기본 보기와 플라이아웃 창에서 각각 <span class="codeph"> s7flyoutzoomview</span> 및 <span class="codeph"> s7flyoutzoom</span> CSS 클래스의 배경이나 유사한 CSS 속성을 사용하여 이미지 주위에 표시되는 추가 공백을 구성할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

선택적.

## 기본값 {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,-1,1`

## 예 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`zoomfactor=2,3,0`
