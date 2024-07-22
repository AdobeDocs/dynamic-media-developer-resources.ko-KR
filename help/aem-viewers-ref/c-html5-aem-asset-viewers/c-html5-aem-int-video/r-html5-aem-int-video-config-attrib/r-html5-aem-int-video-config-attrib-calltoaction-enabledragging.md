---
title: CallToAction.enabledragging
description: 대화형 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 21db58df-b76e-4a78-afc4-5e0188cb8896
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 3%

---

# CallToAction.enabledragging{#calltoaction-enabledragging}

대화형 비디오 뷰어에 대한 구성 속성입니다.

` [CallToAction.|<containerId>_callToAction.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> 사용자가 마우스나 터치 제스처를 사용하여 썸네일을 스크롤하는 기능을 활성화하거나 비활성화합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> overdragvalue </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 0-1 </span> 범위에 있으며 실제 속도와 반대 방향의 이동에 대한 퍼센트 값입니다. </p> <p><span class="codeph"> 1 </span>(으)로 설정된 경우 마우스와 함께 이동합니다. </p> <p><span class="codeph"> 0 </span>(으)로 설정하면 잘못된 방향으로 이동할 수 없습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택적.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`1,0.5`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
enabledragging=0
```
