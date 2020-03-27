---
description: 널
seo-description: 널
seo-title: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
topic: Dynamic media
uuid: e029173b-c004-4be8-b304-d6e2183314ad
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|페이드 </span> </p> </td> 
   <td colname="col2"> <p> 컨트롤 막대와 해당 컨텐츠를 표시하거나 숨기는 데 사용되는 효과 유형을 지정합니다. 아무 <span class="codeph"> 것도 즉시 표시하거나 숨길 </span> 수 없습니다.페이드는 점진적인 페이드 인 및 페이드 아웃 효과를 <span class="codeph"> </span> 제공합니다(Internet Explorer 8에서는 지원되지 않음). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide </span></span> </p> </td> 
   <td colname="col2"> <p> 컨트롤 막대가 등록하는 마지막 마우스/터치 이벤트와 시간 컨트롤 막대가 숨기는 시간 사이의 시간(초)을 지정합니다. </p> <p> - <span class="codeph"> 1로 설정하면 구성 </span> 요소는 자동 숨기기 효과를 트리거하지 않고 항상 화면에 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 기간 </span></span> </p> </td> 
   <td colname="col2"> <p> 페이드 인 및 페이드 아웃 애니메이션의 지속 시간(초)을 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택 사항입니다. 이 명령은 터치 장치에서 무시되며 컨트롤 막대 자동 숨김을 사용할 수 없습니다.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`transition=none`
