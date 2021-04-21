---
description: 기본 보기 영역은 확대/축소 이미지 및 색상 견본으로 차지하는 영역입니다. 일반적으로 크기를 지정하지 않으면 사용 가능한 장치 화면에 맞게 설정됩니다.
solution: Experience Manager
title: 기본 뷰어 영역
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 1%

---


# 기본 뷰어 영역{#main-viewer-area}

기본 보기 영역은 확대/축소 이미지 및 색상 견본으로 차지하는 영역입니다. 일반적으로 크기를 지정하지 않으면 사용 가능한 장치 화면에 맞게 설정됩니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

내장 모드에서 작업할 때(기본 뷰어 영역에 명시적 크기가 주어질 때) 뷰어는 단일 이미지를 사용하여 작업할 때 견본 구성 요소의 높이로 기본 영역의 높이를 자동으로 감소하므로 견본은 필요하지 않습니다.

**기본 뷰어 영역의 CSS 속성**

보기 영역의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7zoomviewer
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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>뷰어의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>뷰어의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 16진수 형식의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 흰색 배경( `#FFFFFF`)을 사용하여 뷰어를 설정하고 크기를 512 x 288픽셀로 지정하려면

```
.s7zoomviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

