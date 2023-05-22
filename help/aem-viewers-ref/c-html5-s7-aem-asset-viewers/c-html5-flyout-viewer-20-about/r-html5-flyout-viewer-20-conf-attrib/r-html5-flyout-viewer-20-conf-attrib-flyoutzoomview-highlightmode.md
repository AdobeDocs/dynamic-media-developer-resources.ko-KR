---
title: FlyoutZoomView.highlightmode
description: FlyoutZoomView.highlightmode
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: b35285a2-7319-4ed7-9681-12a6acda8fa5
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 1%

---

# FlyoutZoomView.highlightmode{#flyoutzoomview-highlightmode}

` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`showtime`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 강조 표시|커서 </span> </p> </td> 
   <td colname="col2"> <p> 사용할 탐색 프레임의 유형을 지정합니다. 로 설정된 경우 <span class="codeph"> 커서 </span>, 구성 요소는 고정 크기 참조 커서를 사용합니다. 데스크탑 시스템 및 터치 장치에 대한 서로 다른 커서 아트를 가질 수 있다. 이 기능은 를 사용하여 제어합니다. <span class="codeph"> .s7cursor </span> CSS 클래스 및 <span class="codeph"> 입력=마우스|터치 </span> 속성 선택기입니다. 데스크탑 시스템에서는 앵커 점이 커서 영역의 중간에 설정되어 있고 터치 장치에서는 앵커 가 커서의 하단 중앙에 있습니다. 로 설정된 경우 <span class="codeph"> 강조 </span>, 구성 요소는 가변 크기의 탐색 프레임을 사용합니다. 프레임의 크기와 모양은 확대/축소 비율 및 플라이아웃 보기의 크기에 따라 다릅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime </span> </span> </p> </td> 
   <td colname="col2"> <p> 사용자가 강조 표시 또는 커서를 활성화한 후 페이드 인하는 데 소요되는 시간(초)을 설정합니다. 페이드 인은 터치 장치에서만 적용되며, 데스크탑 시스템에서는 구성 요소에서 무시됩니다. </p> <p>페이드 인은 다음과 같은 UI 요소에 적용됩니다. 강조 표시 프레임, 고정 커서, 오버레이(이 경우) <span class="codeph"> 오버레이 </span> 매개 변수가 로 설정되어 있습니다. <span class="codeph"> 1 </span>). 플라이아웃 보기 애니메이션은 애니메이션이 완료된 후 강조/커서 페이드 인이 완료된 후에만 시작됩니다. 페이드 아웃 애니메이션은 없습니다. 사용자가 플라이아웃을 비활성화하면 해당 UI 요소(커서, 강조 표시 및 오버레이)가 즉시 숨겨집니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> onimage|free </span> </p> </td> 
   <td colname="col2"> <p> 탐색 프레임 위치를 제어합니다. </p> <p>로 설정된 경우 <span class="codeph"> onimage </span>에서는 탐색 프레임을 기본 보기 내의 실제 이미지 영역 내부에만 배치할 수 있습니다. </p> <p>로 설정된 경우 <span class="codeph"> 무료 </span> 사용자는 이미지 컨텐츠 외부에서도 논리 기본 보기 영역의 아무 곳에나 탐색 프레임을 이동할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

선택적.

## 기본값 {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## 예 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
