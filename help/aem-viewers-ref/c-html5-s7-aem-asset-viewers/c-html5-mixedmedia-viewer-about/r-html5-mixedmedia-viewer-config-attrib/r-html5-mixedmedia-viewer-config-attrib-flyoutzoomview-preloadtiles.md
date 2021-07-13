---
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
title: FlyoutZoomView.preloadtiles
feature: Dynamic Media Classic,Viewers,SDK/API,혼합 미디어 집합
role: Developer,User
exl-id: 041df5c7-9391-4dde-8988-a83272c7c438
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 6%

---

# FlyoutZoomView.preloadtiles{#flyoutzoomview-preloadtiles}

`[FlyoutZoomView.|<containerId>_flyout.]preloadtiles=0|1`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 확대/축소된 이미지를 미리 로드할 수 있도록 <span class="codeph"> 1</span>로 설정하십시오. </p> <p>필요에 따라 <span class="codeph"> 0</span>로 설정하여 확대/축소 이미지를 점진적으로 로드합니다. </p> <p> <p>참고:  이 옵션을 활성화하면 확대/축소 작업을 수행하지 않더라도 확대/축소 이미지를 전체적으로 로드해야 하므로 대역폭 사용이 상당히 증가할 수 있습니다. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preloadtiles=1`
