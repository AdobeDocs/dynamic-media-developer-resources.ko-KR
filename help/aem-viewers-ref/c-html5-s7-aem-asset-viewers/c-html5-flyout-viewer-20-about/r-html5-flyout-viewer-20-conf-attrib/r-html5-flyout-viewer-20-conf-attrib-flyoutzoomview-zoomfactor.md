---
description: 널
seo-description: 널
seo-title: FlyoutZoomView.zoomfactor
solution: Experience Manager
title: FlyoutZoomView.zoomfactor
topic: Dynamic media
uuid: 58d49de7-4828-46ae-b2e7-eb9398e98a99
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *``*[,[ *``*][, *`primaryFactorsecondaryFactorofficient`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 기본 <span class="varname"> 요소</span></span> </p> </td> 
   <td colname="col2"> <p> 기본 보기를 기준으로 플라이아웃 보기의 이미지 배율을 지정합니다.정수 또는 부동 소수점 값 <span class="codeph"> 1.0</span> 이상이어야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 보조</span> 계수 </span> </p> </td> 
   <td colname="col2"> <p> 선택적인 보조 요소는 강조 표시가 활성 상태일 때 기본 보기를 클릭하거나 탭하여 액세스할 수 있도록 지정할 수 있습니다. 두 번째 시간을 클릭하거나 탭하면 기본 확대/축소 요소로 돌아갑니다. 값이 <span class="codeph"> -1이면</span> 보조 확대/축소 인수가 비활성화됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 확대</span></span> </p> </td> 
   <td colname="col2"> <p>구성 요소가 작은 이미지를 처리하는 방식을 지정합니다. </p> <p>1 <span class="codeph"> 로</span> 설정하면 기본 이미지에 맞게 기본 이미지의 크기를 조정합니다. 또한, 구성된 플라이아웃 창 영역을 완전히 채우도록 확대/축소 이미지의 크기를 조정합니다. </p> <p>0으로 <span class="codeph"></span> 설정하면 원본 해상도에 표시되고 기본 보기 영역과 플라이아웃 창 내부에 가운데에 표시됩니다. 기본 보기 및 플라이아웃 창에서 <span class="codeph"> s7flyoutzoomview 및</span> s7flyoutzoom <span class="codeph"></span> CSS 클래스의 배경 또는 유사한 CSS 속성을 사용하여 이미지 주위에 표시되는 추가 공백을 각각 구성할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

선택 사항입니다.

## 기본값 {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,-1,1`

## 예 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`zoomfactor=2,3,0`
