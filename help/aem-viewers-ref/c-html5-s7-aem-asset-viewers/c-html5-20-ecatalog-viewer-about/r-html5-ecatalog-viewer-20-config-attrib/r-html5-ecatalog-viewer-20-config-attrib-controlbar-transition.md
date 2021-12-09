---
title: ControlBar.transition
description: 컨트롤 막대와 해당 콘텐츠를 표시하거나 숨기는 데 사용되는 효과 유형을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: abe8affb-cbcd-4072-b2ed-91a398b1d678
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`기간`*]`

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|페이드 </span> </p> </td> 
   <td colname="col2"> <p> 컨트롤 막대와 해당 콘텐츠를 표시하거나 숨기는 데 사용되는 효과 유형을 지정합니다. 사용 <span class="codeph"> 없음 </span> 즉시 보여주고 숨기려고 <span class="codeph"> 페이드 </span> 점진적 페이드 인 및 페이드 아웃 효과를 제공합니다(Internet Explorer 8에서는 지원되지 않음). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide </span> </span> </p> </td> 
   <td colname="col2"> <p> 컨트롤 막대가 등록하는 마지막 마우스/터치 이벤트와 시간 컨트롤 막대의 숨김 사이의 시간(초)을 지정합니다. </p> <p> 로 설정된 경우 <span class="codeph"> -1 </span>로 지정하는 경우 구성 요소는 자동 숨기기 효과를 트리거하지 않고 항상 화면에 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 기간 </span> </span> </p> </td> 
   <td colname="col2"> <p> 페이드 인 및 페이드 아웃 애니메이션의 지속 시간을 초 단위로 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택 사항입니다. 터치 장치에서는 이 명령이 무시되며, 터치 장치에서는 컨트롤 막대가 자동 숨김을 사용하지 않습니다.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`transition=none`
