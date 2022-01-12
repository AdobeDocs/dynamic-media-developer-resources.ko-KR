---
title: FlyoutZoomView.flyouttransition
description: FlyoutZoomView.flyouttransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 3199d4a3-4799-40a2-b0a5-0e1ee4744fbe
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 3%

---

# FlyoutZoomView.flyouttransition{#flyoutzoomview-flyouttransition}

` [FlyoutZoomView.|<containerId>_flyout.]flyouttransition=[none|slide|fade][, *`showtime`*[, *`showdelay`*[, *`숨기기 시간`*[, *`히데지연`*]]]]`

<table id="table_AB421835D2454ECD8AA40DBFADBAC65F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 없음|슬라이드|페이드 </span> </span> </p> </td> 
   <td colname="col2"> <p> 플라이아웃 보기가 표시되거나 숨겨질 때 적용되는 효과를 지정합니다. 사용 <span class="codeph"> 없음 </span>을 지정하면 활성화되고 준비되면 플라이아웃 이미지가 즉시 나타납니다. <span class="codeph"> 슬라이드 </span> 슬라이드 애니메이션을 왼쪽에서 오른쪽 방향으로 재생합니다. <span class="codeph"> 페이드 </span> 플라이아웃 이미지에 알파 전환을 적용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime </span> </span> </p> </td> 
   <td colname="col2"> <p> 표시 애니메이션을 완료하는 데 걸리는 시간(초)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showdelay </span> </span> </p> </td> 
   <td colname="col2"> <p> 애니메이션 표시를 시작하는 사용자 작업과 애니메이션 자체의 시작 사이의 지연 시간(초)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 숨기기 시간 </span> </span> </p> </td> 
   <td colname="col2"> <p> 숨기기 애니메이션을 완료하는 데 걸리는 시간(초)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 히데지연 </span> </span> </p> </td> 
   <td colname="col2"> <p> 애니메이션 숨기기와 애니메이션 자체를 숨기는 사용자 작업 사이의 지연 시간(초)입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-e6310c8c4e8547689a5b48ceddb3671d}

선택 사항입니다.

## 기본값 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`fade,1,0,1,0`

## 예 {#section-3a188ab955c445bcb2efa3c49722c10d}

`flyouttransition=slide,1,1,2,1`
