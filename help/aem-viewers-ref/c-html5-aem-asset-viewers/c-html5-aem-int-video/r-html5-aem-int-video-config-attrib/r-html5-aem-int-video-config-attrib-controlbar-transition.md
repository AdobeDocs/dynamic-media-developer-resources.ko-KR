---
description: 대화형 비디오 뷰어에 대한 구성 속성입니다.
seo-description: 대화형 비디오 뷰어에 대한 구성 속성입니다.
seo-title: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
topic: Dynamic media
uuid: cde4a5b9-4512-41a6-84ce-9f4fc2cc0399
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# ControlBar.transition{#controlbar-transition}

대화형 비디오 뷰어에 대한 구성 속성입니다.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|페이드</span> </p> </td> 
   <td colname="col2"> <p> 컨트롤 막대와 해당 내용을 표시하거나 숨기는 데 사용할 효과 유형을 지정합니다. </p> <p>즉시 표시/숨기기를 위해 <span class="codeph"> 없음을</span> 설정합니다. </p> <p>점진적인 페이드 인/아웃 효과를 제공하도록 <span class="codeph"> 페이드를</span> 설정합니다. Internet Explorer 8에서는 지원되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> 컨트롤 막대에서 등록한 마지막 마우스/터치 이벤트와 시간 컨트롤 막대가 숨기는 시간 사이의 시간(초)을 지정합니다. -1 <span class="codeph"> 로</span> 설정하면 구성 요소가 자동 숨기기 효과를 트리거하지 않으므로 화면에 항상 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 지속 시간</span></span> </p> </td> 
   <td colname="col2"> <p> 페이드 인/아웃 애니메이션의 지속 시간(초)을 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.5`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```

