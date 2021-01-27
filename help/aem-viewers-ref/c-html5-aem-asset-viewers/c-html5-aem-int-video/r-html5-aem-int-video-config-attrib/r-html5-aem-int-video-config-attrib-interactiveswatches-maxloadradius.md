---
description: 대화형 비디오 뷰어에 대한 구성 속성입니다.
seo-description: 대화형 비디오 뷰어에 대한 구성 속성입니다.
seo-title: InteractiveSwatches.maxloadradius
solution: Experience Manager
title: InteractiveSwatches.maxloadradius
topic: Dynamic Media
uuid: 12391b8b-532f-4e68-ad60-4dbcc86d9e58
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 5%

---


# InteractiveSwatches.maxloadradius{#interactiveswatches-maxloadradius}

대화형 비디오 뷰어에 대한 구성 속성입니다.

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> 구성 요소 미리 로드 동작을 지정합니다. </p> <p><span class="codeph"> -1</span>으로 설정하면 구성 요소가 초기화되거나 자산이 변경될 때 모든 견본이 동시에 로드됩니다. </p> <p><span class="codeph"> 0</span>으로 설정하면 보이는 견본만 로드됩니다. </p> <p>표시 영역 주위에 미리 로드되는 보이지 않는 행/열 수를 정의하려면 <span class="codeph"><span class="varname"> preloadnbr</span></span>로 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`1`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
maxloadradius=-1
```

