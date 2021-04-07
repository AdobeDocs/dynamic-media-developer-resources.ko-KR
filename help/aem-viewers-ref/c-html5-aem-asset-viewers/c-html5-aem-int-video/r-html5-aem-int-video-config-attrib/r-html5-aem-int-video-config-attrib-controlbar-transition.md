---
description: 대화형 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic,뷰어,SDK/API,대화형 비디오
role: 개발자,비즈니스 전문가
exl-id: a8bb32b4-0fd9-4887-98ef-31c3426092b6
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# ControlBar.transition{#controlbar-transition}

대화형 비디오 뷰어에 대한 구성 속성입니다.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|페이드</span> </p> </td> 
   <td colname="col2"> <p> 컨트롤 막대와 해당 내용을 표시하거나 숨기는 데 사용할 효과 유형을 지정합니다. </p> <p>즉시 표시/숨기기를 위해 <span class="codeph"> none</span>으로 설정합니다. </p> <p>점진적 페이드 인/아웃 효과를 제공하려면 <span class="codeph"> 페이드</span>로 설정합니다. Internet Explorer 8에서는 지원되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> 제어 막대에 등록된 마지막 마우스/터치 이벤트와 시간 제어 막대가 숨겨지는 시간(초)을 지정합니다. <span class="codeph"> -1</span>으로 설정하면 구성 요소가 자동 숨기기 효과를 트리거하지 않으므로 항상 화면에 표시됩니다. </p> </td> 
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
