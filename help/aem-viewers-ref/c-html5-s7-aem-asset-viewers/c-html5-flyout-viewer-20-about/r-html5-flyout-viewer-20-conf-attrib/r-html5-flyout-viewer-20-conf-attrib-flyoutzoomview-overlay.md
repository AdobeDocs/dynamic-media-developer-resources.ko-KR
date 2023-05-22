---
title: FlyoutZoomView.overlay
description: FlyoutZoomView.overlay
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 7fbf24c6-900f-4e94-b879-3a8f95dc5c08
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 3%

---

# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 플라이아웃이 활성 상태일 때 기본 보기 강조 표시 모양을 제어합니다. 로 설정된 경우 <span class="codeph"> 0</span>: 현재 플라이아웃 창에 표시되는 영역은에서 제공하는 스타일을 사용하여 강조 표시됩니다. <span class="codeph"> .s7highlight</span> 또는 <span class="codeph"> .s7cursor</span> CSS 클래스 이름(값에 따라 다름) <span class="codeph"> highlightmode</span> 수정자). 로 설정된 경우 <span class="codeph"> 1</span> 구성 요소가 현재 표시된 영역이 완전히 투명한 "반전" 모드로 전환됩니다(이 경우 <span class="codeph"> highlightmode</span> 이(가) (으)로 설정됨 <span class="codeph"> 강조</span>) 또는 로 스타일링 <span class="codeph"> .s7cursor</span> CSS 클래스 이름(대/소문자) <span class="codeph"> highlightmode</span> 이(가) (으)로 설정됨 <span class="codeph"> 커서</span>)에 의해 제공되는 스타일을 사용하여 주변 영역을 채웁니다. <span class="codeph"> .s7overlay</span> CSS 클래스 이름입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

선택적.

## 기본값 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 예 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
