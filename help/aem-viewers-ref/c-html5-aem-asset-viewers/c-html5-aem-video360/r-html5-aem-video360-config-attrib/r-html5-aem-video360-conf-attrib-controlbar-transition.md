---
description: Video360 뷰어에 대한 구성 속성입니다.
seo-description: Video360 뷰어에 대한 구성 속성입니다.
seo-title: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
topic: Dynamic media
uuid: e8c1da96-3533-4d31-9ad3-569a87948ac6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 3%

---


# ControlBar.transition{#controlbar-transition}

Video360 뷰어에 대한 구성 속성입니다.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|페이드</span> </p> </td> 
   <td colname="col2"> <p> 컨트롤 막대와 해당 내용을 표시하거나 숨기는 데 사용되는 효과 유형을 지정합니다. </p> <p><span class="codeph"> none</span>을 사용하여 즉시 표시하고 숨깁니다. 점진적 페이드 인 및 페이드 아웃 효과를 제공하려면 <span class="codeph"> 페이드</span>를 사용합니다. </p> <p>페이드는 Internet Explorer 8에서 지원되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span> </span> </p> </td> 
   <td colname="col2"> <p>컨트롤 막대가 등록하는 마지막 마우스/터치 이벤트와 시간 컨트롤 막대가 숨겨지는 시간(초)을 지정합니다. </p> <p> <span class="codeph"> -1</span>으로 설정하면 구성 요소는 자동 숨기기 효과를 트리거하지 않으며 항상 화면에 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 지속 시간</span> </span> </p> </td> 
   <td colname="col2"> <p>페이드 인 및 페이드 아웃 애니메이션의 지속 시간(초)을 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택 사항입니다.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
transition=none
```

