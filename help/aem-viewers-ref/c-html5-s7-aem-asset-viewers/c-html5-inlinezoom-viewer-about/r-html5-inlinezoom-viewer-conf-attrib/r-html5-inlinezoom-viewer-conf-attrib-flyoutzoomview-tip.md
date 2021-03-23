---
description: FlyoutZoomView.tip
solution: Experience Manager
title: FlyoutZoomView.tip
uuid: 42bbef39-36b6-4f1d-a228-0aaf107600a9
feature: Dynamic Media Classic,뷰어,SDK/API,인라인 확대/축소
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 3%

---


# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *``*[, *``*][, *`지속 시간`*]`

<table id="table_3BA079B51B644219BB8E2A68A13A8D90"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 지속 시간</span> </span> </p> </td> 
   <td colname="col2"> <p>팁 텍스트가 숨겨지기 전에 표시되는 시간(초)을 지정합니다. <span class="codeph"> -1</span>으로 설정하면 사용자가 플라이아웃을 활성화해도 항상 메시지가 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span> </span> </p> </td> 
   <td colname="col2"> <p>세트에서 새 이미지를 볼 때 텍스트가 표시되는 횟수를 지정합니다. <span class="codeph"> -1</span> 값은 세트에서 이미지를 볼 때 텍스트가 항상 표시됨을 의미합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 페이드</span> </span> </p> </td> 
   <td colname="col2"> <p>텍스트가 나타나거나 사라질 때 발생하는 페이드 애니메이션의 지속 시간을 지정합니다. <span class="codeph"> 0</span> 값은 페이드 전환이 없음을 의미합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-e6310c8c4e8547689a5b48ceddb3671d}

선택 사항입니다.

## 기본값 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,1,0.3`

## 예 {#section-3a188ab955c445bcb2efa3c49722c10d}

`tip=1,-1,0`
