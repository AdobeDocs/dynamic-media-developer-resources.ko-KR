---
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
title: FlyoutZoomView.zoomfactor
topic: Dynamic media
uuid: 8c4e6bf8-0238-470b-9fbe-262eb17f8f3b
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---


# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *``*[,[ *``*][, *`primaryFactorsecondaryFactoruphale`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> 기본 보기를 기준으로 플라이아웃 보기의 이미지 배율을 지정합니다.정수 또는 부동 소수점 값 <span class="codeph"> 1.0</span> 이상이어야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> 선택적인 보조 요소는 강조 표시가 활성 상태일 때 기본 보기를 클릭하거나 탭하여 액세스할 수 있습니다. 두 번째 시간을 클릭하거나 탭하면 기본 확대/축소 요소로 되돌아갑니다. <span class="codeph"> -1</span> 값은 보조 확대/축소 인수를 비활성화합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 확대</span></span> </p> </td> 
   <td colname="col2"> <p>구성 요소가 작은 이미지를 처리하는 방식을 지정합니다. </p> <p><span class="codeph"> 1</span>으로 설정된 경우 구성 요소는 기본 보기에 맞도록 기본 이미지의 크기를 조정합니다. 또한, 구성된 플라이아웃 창 영역을 완전히 채우도록 확대/축소 이미지의 크기를 확대합니다. </p> <p><span class="codeph"> 0</span>으로 설정하면 작은 이미지가 원래 해상도로 표시되고 기본 보기 영역과 플라이아웃 창 내부에 표시됩니다. 기본 보기 및 플라이아웃 창에서 각각 <span class="codeph"> s7flyoutzoomview</span> 및 <span class="codeph"> s7flyoutzoom</span> CSS 클래스의 배경 또는 유사한 CSS 속성을 사용하여 이미지 주위의 추가 공백을 구성할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-e6310c8c4e8547689a5b48ceddb3671d}

선택 사항입니다.

## 기본값 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,-1,1`

## 예 {#section-3a188ab955c445bcb2efa3c49722c10d}

`zoomfactor=2,3,0`
