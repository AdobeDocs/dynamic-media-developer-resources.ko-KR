---
description: ZoomView.frametransition
solution: Experience Manager
title: ZoomView.frametransition
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 4%

---


# ZoomView.frametransition{#zoomview-frametransition}

` [ZoomView.|<containerId>_zoomView.]frametransition=none|fade|slide[, *``*[, *`지속 시간 간격`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|페이드|슬라이드  </span> </p> </td> 
   <td colname="col2"> <p>프레임 변경에 적용된 효과의 유형을 지정합니다. <span class="codeph"> 어느  </span> 것도 전환을 의미하지 않으며 프레임 변경은 즉시 발생합니다. <span class="codeph"> 페이드 </span> 는 이전 프레임과 새 프레임 사이의 크로스 페이드 전환을 의미합니다. <span class="codeph"> 슬라이드를  </span> 활성화하면 이전 프레임이 보기에서 미끄러지고 새 프레임 슬라이드가 들어오는 전환이 활성화됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 지속 시간  </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 페이드 </span> 또는 <span class="codeph"> 슬라이드 </span> 전환 효과의 지속 시간(초)을 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 간격  </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 슬라이드 </span> 전환에서 인접한 프레임 사이의 간격은 <span class="codeph"> 0 </span>과 <span class="codeph"> 1 </span> 사이의 범위를 가지며 구성 요소의 폭을 기준으로 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

없음.

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,1`
