---
title: ControlBar.transition
description: 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 133717c7-38d9-47b6-86bb-e23ebd8f147a
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

비디오 뷰어에 대한 구성 속성입니다.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`지연 숨기기`*[, *`지속 시간`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|페이드</span> </p> </td> 
   <td colname="col2"> <p> 컨트롤 막대 및 해당 내용을 표시하거나 숨기는 데 사용할 효과 유형을 지정합니다. </p> <p>사용 <span class="codeph"> 없음</span> 즉시 표시하거나 숨길 수 있습니다. 사용 <span class="codeph"> 페이드</span> 점진적인 페이드 인 및 페이드 아웃 효과를 제공합니다. </p> <p>페이드는 Internet Explorer 8에서 지원되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 지연 숨기기</span> </span> </p> </td> 
   <td colname="col2"> <p>컨트롤 막대가 등록한 마지막 마우스/터치 이벤트와 컨트롤 막대가 숨기는 시간(초)을 지정합니다. </p> <p> 로 설정된 경우 <span class="codeph"> -1</span>, 구성 요소가 자동 숨기기 효과를 트리거하지 않고 항상 화면에서 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 지속 시간</span> </span> </p> </td> 
   <td colname="col2"> <p>페이드 인 및 페이드 아웃 애니메이션의 지속 시간(초)을 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택적.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
transition=none
```
