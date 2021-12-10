---
title: ZoomView.frametransition
description: ZoomView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: f57a8a2e-63a1-4a59-9a25-b435d0ac39dc
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 5%

---

# ZoomView.frametransition{#zoomview-frametransition}

` [ZoomView.|<containerId>_zoomView.]frametransition=none|fade|slide[, *`기간`*[, *`간격`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|페이드|슬라이드 </span> </p> </td> 
   <td colname="col2"> <p>프레임 변경에 적용되는 효과의 유형을 지정합니다. 속성 <span class="codeph"> 없음 </span> 전환하지 않을 것을 의미합니다. 프레임 변경은 즉시 발생합니다. 속성 <span class="codeph"> 페이드 </span> 는 이전 프레임과 새 프레임 간에 교차 페이드 전환을 의미합니다. 속성 <span class="codeph"> 슬라이드 </span> 이전 프레임이 보기에서 슬라이딩되고 새 프레임이 슬라이딩되는 전환을 활성화합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 기간 </span> </span> </p> </td> 
   <td colname="col2"> <p>다음 기간(초)을 지정합니다 <span class="codeph"> 페이드 </span> 또는 <span class="codeph"> 슬라이드 </span> 전환 효과. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 간격 </span> </span> </p> </td> 
   <td colname="col2"> <p>인접한 프레임 사이의 간격 <span class="codeph"> 슬라이드 </span> 전환, 다음 범위의 <span class="codeph"> 0 </span> through <span class="codeph"> 1 </span> 및 은 구성 요소의 너비를 기준으로 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

없음.

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,1`
