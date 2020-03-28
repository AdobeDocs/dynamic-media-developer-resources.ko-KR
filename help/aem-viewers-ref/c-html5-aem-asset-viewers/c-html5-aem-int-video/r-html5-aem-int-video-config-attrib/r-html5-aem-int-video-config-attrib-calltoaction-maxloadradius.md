---
description: 대화형 비디오 뷰어에 대한 구성 속성입니다.
seo-description: 대화형 비디오 뷰어에 대한 구성 속성입니다.
seo-title: CallToAction.maxloadradius
solution: Experience Manager
title: CallToAction.maxloadradius
topic: Dynamic media
uuid: ec5a4b0d-1dae-456f-a9da-91541cfba1a7
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# CallToAction.maxloadradius{#calltoaction-maxloadradius}

대화형 비디오 뷰어에 대한 구성 속성입니다.

` [CallToAction.|<containerId>_callToAction.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> 구성 요소 미리 로드 동작을 지정합니다. </p> <p>-1 <span class="codeph"> 로</span> 설정하면 구성 요소가 초기화되거나 자산이 변경될 때 모든 축소판이 동시에 로드됩니다. </p> <p>0으로 설정하면 <span class="codeph"></span> 보이는 축소판만 로드됩니다. </p> <p>표시 영역 주위의 보이지 않는 행/열 수를 <span class="codeph"><span class="varname"> 미리</span></span> 로드하도록 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`-1`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
maxloadradius=-1
```

