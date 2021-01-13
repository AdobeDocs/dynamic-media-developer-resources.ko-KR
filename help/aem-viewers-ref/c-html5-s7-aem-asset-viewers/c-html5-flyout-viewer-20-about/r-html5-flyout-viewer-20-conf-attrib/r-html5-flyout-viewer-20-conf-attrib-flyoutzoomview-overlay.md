---
description: FlyoutZoomView.overlay
solution: Experience Manager
title: FlyoutZoomView.overlay
topic: Dynamic media
uuid: e6e9e97c-5d9b-47ca-bae3-ed3371c5ff9b
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 4%

---


# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 플라이아웃이 활성 상태일 때 기본 보기 강조 표시 모양을 제어합니다. <span class="codeph"> 0</span>으로 설정하면 플라이아웃 창에 현재 표시되는 영역이 <span class="codeph"> .s7highlight</span> 또는 <span class="codeph"> .s7cursor</span> CSS 클래스 이름( <span class="codeph"> highlightmode</span> 수정자 값에 따라)에서 제공하는 스타일을 사용하여 강조 표시됩니다. <span class="codeph"> 1</span> 구성 요소로 설정하면 현재 표시된 영역이 완전히 투명하게(예: <span class="codeph"> highlightmode</span>이(가) <span class="codeph"> highlight</span>로 설정됨) 또는 <span class="codeph"> .s7cursor</span> CSS 클래스 이름(예: <span class="codeph"> hightlightmode</span>가 있음)으로 스타일이 지정된 경우) <span class="codeph"> 커서</span>)로 설정되었지만, 주변 영역은 <span class="codeph"> .s7overlay</span> CSS 클래스 이름으로 제공되는 스타일을 사용하여 채워집니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

선택 사항입니다.

## 기본값 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 예 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
