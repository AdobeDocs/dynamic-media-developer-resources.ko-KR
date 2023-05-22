---
title: 포커스 강조 표시
description: 포커스가 있는 뷰어 UI 요소 주위에 표시되는 입력 포커스 강조 표시는 CSS 클래스 선택기로 제어됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 31fd8022-0072-4a4c-8947-57858a094f3c
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---

# 포커스 강조 표시{#focus-highlight}

포커스가 있는 뷰어 UI 요소 주위에 표시되는 입력 포커스 강조 표시는 CSS 클래스 선택기로 제어됩니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS 속성**

다음 CSS 클래스 선택기를 사용하여 모양이 제어됩니다.

```
.s7zoomviewer *:focus
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
   <td colname="col1"> <p> <span class="codeph"> 개요 </span> </p> </td> 
   <td colname="col2"> <p>포커스 강조 표시 스타일입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 모든 뷰어 사용자 인터페이스 요소에 대해 기본 브라우저 포커스 강조 표시를 비활성화하려면 다음 CSS 선택기를 뷰어의 스타일 시트에 추가하십시오.

```
.s7zoomviewer *:focus { 
 outline: none; 
}
```
