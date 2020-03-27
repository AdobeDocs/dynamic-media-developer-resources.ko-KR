---
description: 대화형 비디오 뷰어에 대한 구성 속성입니다.
seo-description: 대화형 비디오 뷰어에 대한 구성 속성입니다.
seo-title: CallToAction.enabledragging
solution: Experience Manager
title: CallToAction.enabledragging
topic: Dynamic media
uuid: efb272b5-e30e-44d5-9dec-0529b1074ed2
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# CallToAction.enabledragging{#calltoaction-enabledragging}

대화형 비디오 뷰어에 대한 구성 속성입니다.

` [CallToAction.|<containerId>_callToAction.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 사용자가 마우스로 축소판을 스크롤하거나 터치 제스처를 사용하여 축소판을 스크롤할 수 있도록 하거나 비활성화할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> overdragvalue </span></span> </p> </td> 
   <td colname="col2"> <p> 이 <span class="codeph"> 0-1 </span> 범위에 있고 실제 속도의 잘못된 방향으로 이동을 위한 백분율 값입니다. </p> <p>1로 설정하면 마우스와 함께 <span class="codeph"> </span> 이동합니다. </p> <p>0으로 설정하면 <span class="codeph"> 잘못된 방향으로 이동할 수 </span> 없습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`1,0.5`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
enabledragging=0
```

