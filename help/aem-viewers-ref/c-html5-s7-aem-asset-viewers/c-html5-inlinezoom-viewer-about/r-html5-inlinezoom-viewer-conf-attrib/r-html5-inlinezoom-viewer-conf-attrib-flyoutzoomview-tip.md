---
title: FlyoutZoomView.tip
description: FlyoutZoomView.tip
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: df73235b-547e-4d47-aa76-1d2bd4aead9b
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 3%

---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`지속 시간`*[, *`카운트`*][, *`페이드`*]`

<table id="table_3BA079B51B644219BB8E2A68A13A8D90"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 기간</span> </span> </p> </td> 
   <td colname="col2"> <p>팁 텍스트가 숨겨지기 전에 표시되는 시간(초)을 지정합니다. <span class="codeph"> -1</span>(으)로 설정된 경우 사용자가 플라이아웃을 활성화하더라도 메시지는 항상 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 개수</span> </span> </p> </td> 
   <td colname="col2"> <p>집합에서 새 이미지를 볼 때 텍스트가 표시되는 횟수를 지정합니다. 값 <span class="codeph"> -1</span>은(는) 집합에서 이미지를 볼 때 텍스트가 항상 표시됨을 의미합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 페이드</span> </span> </p> </td> 
   <td colname="col2"> <p>텍스트가 나타나거나 사라질 때 발생하는 페이드 애니메이션의 지속 시간을 지정합니다. <span class="codeph"> 0</span> 값은 페이드 전환이 없음을 의미합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-e6310c8c4e8547689a5b48ceddb3671d}

선택적.

## 기본값 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,1,0.3`

## 예 {#section-3a188ab955c445bcb2efa3c49722c10d}

`tip=1,-1,0`
