---
title: FlyoutZoomView.preloadtiles
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: f50ea45a-afd5-4e4f-967d-c45cecc5fb7b
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 6%

---

# FlyoutZoomView.preloadtiles{#flyoutzoomview-preloadtiles}

`[FlyoutZoomView.|<containerId>_flyout.]preloadtiles=0|1`

<table id="table_8E44EC404A1A45C59EA1EF2766613930"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 다음으로 설정 <span class="codeph"> 1</span> 확대/축소된 이미지의 사전 로드를 활성화하거나 를 로 설정 <span class="codeph"> 0</span> 필요에 따라 확대/축소 이미지를 점진적으로 로드합니다. </p> <p> <p>참고: 이 옵션을 활성화하면 대역폭 사용량이 크게 증가할 수 있습니다. 사용자가 확대/축소 작업을 시작하지 않더라도 확대/축소된 이미지가 전체적으로 로드됩니다. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-e6310c8c4e8547689a5b48ceddb3671d}

선택적.

## 기본값 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`0`

## 예 {#section-3a188ab955c445bcb2efa3c49722c10d}

`preloadtiles=1`
