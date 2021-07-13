---
description: PageView.zoomstep
solution: Experience Manager
title: PageView.zoomstep
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 64cce312-c13b-49c7-af85-3349ff5c4322
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 6%

---

# PageView.zoomstep{#pageview-zoomstep}

` [PageView.|<containerId>_pageView.]zoomstep= *``*[, *`steplimit`*]`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 단계</span></span> </p> </td> 
   <td colname="col2"> <p> 해상도를 두 배수로 늘리거나 줄이는 데 필요한 확대 및 축소 작업 수를 구성합니다. 각 확대/축소 작업에 대한 해상도 변경은 단계당 2^1입니다. 한 번의 확대/축소 작업으로 전체 해상도로 확대하려면 <span class="codeph"> 0</span>로 설정하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 제한</span></span> </p> </td> 
   <td colname="col2"> <p> 전체 해상도 이미지를 기준으로 최대 확대/축소 해상도를 지정합니다. 기본값은 <span class="codeph"> 1.0</span>이며, 이 경우 전체 해상도 이상의 확대/축소를 허용하지 않습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-636d35a4791447039f1902973f568320}

선택 사항입니다.

## 기본값 {#section-ad8a5fe2383e4c228bf177a41b53d921}

`1,1`

## 예 {#section-1e20672d42c845bd84f02f88cbc53efc}

`zoomstep=2,3`
