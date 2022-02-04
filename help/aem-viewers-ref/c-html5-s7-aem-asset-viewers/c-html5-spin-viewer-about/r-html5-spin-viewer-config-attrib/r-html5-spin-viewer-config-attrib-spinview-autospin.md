---
title: SpinView.autospin
description: SpinView.autospin
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 16276e07-5494-4fd9-bd77-e77a46c57fd1
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 7%

---

# SpinView.autospin{#spinview-autospin}

` [SpinView.|<containerId>_spinView.]maxloadradius=0|1[, *`기간`*][, *`방향`*][, *`spin_number`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 자동 스핀 애니메이션을 활성화하거나 비활성화합니다. 최상의 자동 회전 경험을 얻으려면 를 설정하여 모든 프레임을 미리 로드하는 것이 좋습니다 <span class="codeph"> maxloadradius</span> to <span class="codeph"> -1</span>. 그러나 이 설정을 사용하면 로드 시간이 증가하고 대역폭 사용량이 증가합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 지속 시간</span></span> </p> </td> 
   <td colname="col2"> <p> 1개의 전체 스핀당 초 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 방향</span></span> </p> </td> 
   <td colname="col2"> <p> 회전 방향 <span class="codeph"> 0</span> 동쪽으로의 회전이 <span class="codeph"> 1</span> 서쪽방입니다 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> spin_number</span></span> </p> </td> 
   <td colname="col2"> <p> 자동 회전이 중지되기 전에 수행되는 전체 회전 수입니다. 숫자는 부동 소수점 숫자입니다. 을 로 설정합니다. <span class="codeph"> -1</span> 무한 자동 회전. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-924163cb2f6542499f49894becef7fb5}

선택 사항입니다.

## 기본값 {#section-7a2128fd488941948aff18421f533ccf}

`0,1,1,1`

## 예 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`autospin=1,2,-1,1`
