---
description: 연속 확대/축소 모드에서는 현재 자산이 단일 이미지일 때 확대/축소 가능한 이미지로 구성됩니다.
seo-description: 연속 확대/축소 모드에서는 현재 자산이 단일 이미지일 때 확대/축소 가능한 이미지로 구성됩니다.
seo-title: 확대/축소 보기
solution: Experience Manager
title: 확대/축소 보기
topic: Dynamic media
uuid: c9113275-eec6-4014-b7ad-3ae9f2cf01d9
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Zoom view{#zoom-view}

연속 확대/축소 모드에서는 현재 자산이 단일 이미지일 때 확대/축소 가능한 이미지로 구성됩니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

보기 영역의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7mixedmediaviewer .s7zoomview
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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 기본 보기의 16진수 형식의 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 커서 </span> </p> </td> 
   <td colname="col2"> <p>기본 보기 위에 커서가 표시됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 확대/축소 보기를 투명하게 만듭니다.

```
.s7mixedmediaviewer .s7zoomview { 
 background-color: transparent; 
}
```

데스크톱 시스템에서 구성 요소는 클래스에 적용할 수 있는 `cursortype` 속성 선택기를 지원합니다 `.s7zoomview` . 구성 요소 상태 및 사용자 작업을 기반으로 커서의 유형을 제어합니다. The following `cursortype` values are supported:

* `default`

   작은 이미지 해상도, 구성 요소 설정 또는 둘 다로 인해 이미지를 확대할 수 없을 때 표시됩니다.

* `zoomin`

   이미지를 확대할 수 있을 때 표시됩니다.

* `reset`

   이미지가 최대 확대/축소 수준에 있을 때 표시되며 초기 상태로 재설정할 수 있습니다.

* `drag`

   사용자가 확대된 상태의 이미지를 이동할 때 표시됩니다.

* `slide`

   사용자가 가로 스와이프 또는 터치를 수행하여 이미지 교환을 수행할 때 표시됩니다.

