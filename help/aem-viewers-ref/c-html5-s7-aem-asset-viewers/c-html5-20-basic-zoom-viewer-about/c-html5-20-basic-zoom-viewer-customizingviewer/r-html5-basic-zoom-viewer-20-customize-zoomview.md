---
title: 확대/축소 보기
description: 기본 보기는 확대/축소 가능한 이미지로 구성됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 286b9df4-88db-4e5d-aab4-9cbe01195e57
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 1%

---

# 확대/축소 보기{#zoom-view}

기본 보기는 확대/축소 가능한 이미지로 구성됩니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

다음 CSS 클래스 선택기를 사용하여 보기 영역의 모양이 제어됩니다.

```
.s7basiczoomviewer .s7zoomview
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p> 기본 보기의 16진수 형식 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 커서 </span> </p> </td> 
   <td colname="col2"> <p>기본 뷰 위에 커서가 표시됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 기본 보기를 투명하게 합니다.

```
.s7basiczoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

데스크톱 시스템에서 구성 요소는 `.s7zoomview` 클래스에 적용할 수 있는 `cursortype` 특성 선택기를 지원하고 구성 요소 상태 및 사용자 작업을 기반으로 커서 형식을 제어합니다. 다음 `cursortype` 값이 지원됩니다.

<table id="table_BC9FC40DA27B4A85995F4E9431AABF33"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>값 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 기본 </span> </p> </td> 
   <td colname="col2"> <p>작은 이미지 해상도, 구성 요소 설정 또는 둘 다로 인해 이미지를 확대/축소할 수 없을 때 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin </span> </p> </td> 
   <td colname="col2"> <p>이미지를 확대할 수 있을 때 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> 재설정 </p> </td> 
   <td colname="col2"> <p>이미지가 최대 확대/축소 레벨에 있고 초기 상태로 재설정할 수 있을 때 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 드래그 </span> </p> </td> 
   <td colname="col2"> <p>사용자가 확대 중인 이미지를 이동할 때 표시됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
