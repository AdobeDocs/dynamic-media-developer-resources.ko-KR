---
description: CarouselView.frametransition
solution: Experience Manager
title: CarouselView.frametransition
feature: Dynamic Media Classic,Viewers,SDK/API,회전 배너
role: Developer,Business Practitioner
exl-id: 771395fb-775d-462e-86dc-0600cfecb345
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 5%

---

# CarouselView.frametransition{#carouselview-frametransition}

` [CarouselView.|<containerId>_carouselView.]frametransition=none|fade|slide[, *``*[, *`지속 시간 간격`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|페이드|슬라이드  </span> </p> </td> 
   <td colname="col2"> <p>프레임 변경에 적용되는 효과의 유형을 지정합니다. <span class="codeph"> 어느  </span> 것도 과도하지 않다.프레임 변경은 즉시 발생합니다. </p> <p> <span class="codeph"> 페이드 </span> 는 이전 프레임과 새 프레임 간에 교차 페이드 전환을 의미합니다. </p> <p> <span class="codeph"> 슬라이드 </span> 가 이전 프레임이 보기에서 슬라이딩되고 새 프레임이 슬라이딩되는 전환을 활성화합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 기간  </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 페이드 </span> 또는 <span class="codeph"> 슬라이드 </span> 전환 효과의 기간(초)을 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 간격  </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 슬라이드 </span> 전환에서 인접한 프레임 사이의 간격은 <span class="codeph"> 0 </span> 및 <span class="codeph"> 1 </span> 사이의 범위이며 구성 요소의 너비를 기준으로 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

없음.

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,0.3`
