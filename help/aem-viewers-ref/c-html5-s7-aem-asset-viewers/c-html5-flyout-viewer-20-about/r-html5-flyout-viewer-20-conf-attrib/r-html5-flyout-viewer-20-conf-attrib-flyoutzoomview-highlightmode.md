---
description: 널
seo-description: 널
seo-title: FlyoutZoomView.highlightmode
solution: Experience Manager
title: FlyoutZoomView.highlightmode
topic: Dynamic media
uuid: 397c1af0-f806-4555-83fa-ec7548b59a60
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.highlightmode{#flyoutzoomview-highlightmode}

` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`showtime`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 강조|커서 </span> </p> </td> 
   <td colname="col2"> <p> 사용할 탐색 프레임의 유형을 지정합니다. 커서로 설정하면 구성 <span class="codeph"> </span>요소는 고정 크기 참조 커서를 사용합니다. 데스크톱 시스템과 터치 장치에 대해 서로 다른 커서 아트를 사용할 수 있습니다. 이 작업은 <span class="codeph"> .s7cursor </span> CSS 클래스와 <span class="codeph"> input=mouse|touch </span> 속성 선택기로 제어됩니다. 데스크톱 시스템에서 기준점은 커서 영역의 중앙에 설정되고 터치 장치의 앵커는 커서의 아래쪽 가운데에 위치합니다. 강조 <span class="codeph"> </span>표시로 설정되면 구성 요소는 가변 크기 탐색 프레임을 사용합니다.프레임의 크기와 모양은 확대/축소 비율과 플라이아웃 보기의 크기에 따라 달라집니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 쇼타임 </span></span> </p> </td> 
   <td colname="col2"> <p> 사용자가 활성화한 후 강조 표시나 커서가 페이드 인되는 시간(초)을 설정합니다. 페이드는 터치 장치에만 적용됩니다.데스크톱 시스템에서는 구성 요소에서 무시됩니다. </p> <p>페이드 인은 다음 UI 요소에 적용됩니다.강조 프레임, 고정 커서, 오버레이( <span class="codeph"> 오버레이 </span> 매개 변수가 <span class="codeph"> 1로 설정된 경우) </span>. 플라이아웃 보기 애니메이션은 애니메이션의 밝은 영역/커서 페이드가 완료된 후에만 시작됩니다. 페이드 아웃 애니메이션은 없습니다. 사용자가 플라이아웃을 비활성화하면 해당 UI 요소(커서, 강조 표시 및 오버레이)가 즉시 숨겨집니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> onimage|free </span> </p> </td> 
   <td colname="col2"> <p> 내비게이션 프레임 위치를 제어합니다. </p> <p>onimage로 <span class="codeph"> 설정된 </span> 경우 탐색 프레임은 기본 보기 내의 실제 이미지 영역 내에만 배치할 수 있습니다. </p> <p>[무료]로 <span class="codeph"> 설정된 </span> 경우 사용자는 이미지 컨텐츠 외부에 있더라도 논리 기본 보기 영역의 아무 곳이나 내비게이션 프레임을 이동할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

선택 사항입니다.

## 기본값 {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## 예 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
