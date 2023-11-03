---
description: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 2e08a62b-9499-41f8-927b-89bed972b4eb
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

[!DNL ` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`지연 숨기기`*[, *`지속 시간`*]`]

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|페이드 </span> </p> </td> 
   <td colname="col2"> <p> 컨트롤 막대 및 해당 내용을 표시하거나 숨기는 데 사용할 효과 유형을 지정합니다. 사용 <span class="codeph"> 없음 </span> 즉시 표시하거나 숨기는 데 사용합니다. <span class="codeph"> 페이드 </span> 에서는 점진적인 페이드 인 및 페이드 아웃 효과를 제공합니다(Internet Explorer 8에서는 지원되지 않음). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 지연 숨기기 </span> </span> </p> </td> 
   <td colname="col2"> <p> 컨트롤 막대가 등록한 마지막 마우스/터치 이벤트와 시간 컨트롤 막대가 숨기는 간격(초)을 지정합니다. </p> <p> 로 설정된 경우 <span class="codeph"> -1 </span> 구성 요소가 자동 숨기기 효과를 트리거하지 않고 항상 화면에서 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 지속 시간 </span> </span> </p> </td> 
   <td colname="col2"> <p> 페이드 인 및 페이드 아웃 애니메이션의 지속 시간(초)을 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택적. 이 명령은 컨트롤 막대 자동 숨기기가 비활성화된 터치 장치에서는 무시됩니다.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `fade,2,0.5`]

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `transition=none`]
