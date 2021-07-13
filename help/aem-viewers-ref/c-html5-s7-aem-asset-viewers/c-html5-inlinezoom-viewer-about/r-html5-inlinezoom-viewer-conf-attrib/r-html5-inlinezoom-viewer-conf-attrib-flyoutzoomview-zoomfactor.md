---
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
title: FlyoutZoomView.zoomfactor
feature: Dynamic Media Classic,Viewers,SDK/API,인라인 확대/축소
role: Developer,User
exl-id: 2a9d4450-a1a0-471c-86bf-105d516b0bd7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 2%

---

# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *``*[,[ *``*][, *``*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> 기본 보기에 상대적인 플라이아웃 보기에 대한 이미지 확대율을 지정합니다. 정수 또는 부동 소수점 값 <span class="codeph"> 1.0</span> 이상이어야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> 강조 표시가 활성 상태일 때 기본 보기를 클릭하거나 탭하여 액세스할 수 있는 선택적 보조 요소를 지정할 수 있습니다. 두 번째 시간을 클릭하거나 탭하면 기본 확대/축소 인자로 되돌아갑니다. <span class="codeph"> -1</span> 값은 보조 확대/축소 인수를 사용하지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 고급</span></span> </p> </td> 
   <td colname="col2"> <p>구성 요소가 작은 이미지를 처리하는 방법을 지정합니다. </p> <p><span class="codeph"> 1</span> 로 설정하면 구성 요소가 기본 보기에 맞도록 기본 이미지를 업스케일링합니다. 또한 구성된 플라이아웃 창 영역을 완전히 채우도록 확대/축소 이미지의 크기를 늘립니다. </p> <p><span class="codeph"> 0</span> 로 설정하면 작은 이미지가 원래 해상도로 표시되고 기본 보기 영역과 플라이아웃 창 내부에 가운데에 표시됩니다. 기본 보기 및 플라이아웃 창에서 각각 <span class="codeph"> s7flyoutzoomview</span> 및 <span class="codeph"> s7flyoutzoom</span> CSS 클래스의 배경 또는 유사한 CSS 속성을 사용하여 이미지 주위에 추가 공백을 구성할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-e6310c8c4e8547689a5b48ceddb3671d}

선택 사항입니다.

## 기본값 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,-1,1`

## 예 {#section-3a188ab955c445bcb2efa3c49722c10d}

`zoomfactor=2,3,0`
