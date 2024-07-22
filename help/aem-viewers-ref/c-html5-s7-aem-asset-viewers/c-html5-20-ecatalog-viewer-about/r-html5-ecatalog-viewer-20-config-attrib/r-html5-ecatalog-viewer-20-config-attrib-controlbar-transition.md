---
title: ControlBar.transition
description: 컨트롤 막대 및 해당 내용을 표시하거나 숨기는 데 사용할 효과 유형을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: abe8affb-cbcd-4072-b2ed-91a398b1d678
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 1%

---

# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`duration`*]`

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|페이드 </span> </p> </td> 
   <td colname="col2"> <p> 컨트롤 막대 및 해당 내용을 표시하거나 숨기는 데 사용할 효과 유형을 지정합니다. 즉시 표시하거나 숨기려면 <span class="codeph"> 없음 </span>을(를) 사용하고, <span class="codeph"> 페이드 인/페이드 아웃 효과를 점진적으로 제공합니다(Internet Explorer 8에서는 지원되지 않음).</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 지연 숨기기 </span> </span> </p> </td> 
   <td colname="col2"> <p> 컨트롤 막대가 등록한 마지막 마우스/터치 이벤트와 시간 컨트롤 막대 숨기기 사이의 시간을 초 단위로 지정합니다. </p> <p> <span class="codeph"> -1 </span>(으)로 설정된 경우 구성 요소가 자동 숨기기 효과를 트리거하지 않고 항상 화면에서 표시 상태를 유지합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 기간 </span> </span> </p> </td> 
   <td colname="col2"> <p> 페이드 인 및 페이드 아웃 애니메이션의 지속 시간(초)을 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택 사항입니다. 이 명령은 컨트롤 막대 자동 숨기기가 비활성화된 터치 장치에서는 무시됩니다.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`transition=none`
