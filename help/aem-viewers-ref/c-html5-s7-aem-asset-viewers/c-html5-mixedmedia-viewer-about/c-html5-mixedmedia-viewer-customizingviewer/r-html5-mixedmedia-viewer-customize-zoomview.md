---
title: 확대/축소 보기
description: 연속 확대/축소 모드에서 기본 보기는 현재 자산이 단일 이미지일 때 확대/축소 가능한 이미지로 구성됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0252436b-ba96-4273-b796-d1772fc093b0
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---

# 확대/축소 보기{#zoom-view}

연속 확대/축소 모드에서 기본 보기는 현재 자산이 단일 이미지일 때 확대/축소 가능한 이미지로 구성됩니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

다음 CSS 클래스 선택기를 사용하여 보기 영역의 모양이 제어됩니다.

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
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p> 기본 보기의 16진수 형식 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 커서 </span> </p> </td> 
   <td colname="col2"> <p>기본 보기에 표시되는 커서입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 확대/축소 보기를 투명하게 만듭니다.

```
.s7mixedmediaviewer .s7zoomview { 
 background-color: transparent; 
}
```

데스크톱 시스템에서 구성 요소는 `.s7zoomview` 클래스에 적용할 수 있는 `cursortype` 특성 선택기를 지원합니다. 구성 요소 상태 및 사용자 작업을 기반으로 커서 유형을 제어합니다. 다음 `cursortype` 값이 지원됩니다.

* `default`

  작은 이미지 해상도, 구성 요소 설정 또는 둘 다로 인해 이미지를 확대/축소할 수 없을 때 표시됩니다.

* `zoomin`

  이미지를 확대할 수 있을 때 표시됩니다.

* `reset`

  이미지가 최대 확대/축소 레벨에 있고 초기 상태로 재설정할 수 있을 때 표시됩니다.

* `drag`

  사용자가 확대 상태인 이미지를 패닝할 때 표시됩니다.

* `slide`

  사용자가 가로 스와이프 또는 긋기를 수행하여 이미지 교체를 수행할 때 표시됩니다.
