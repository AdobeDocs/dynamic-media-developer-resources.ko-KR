---
title: 기본 뷰어 영역
description: 기본 보기 영역은 확대/축소 이미지와 견본이 차지하는 영역입니다. 크기를 지정하지 않은 경우 일반적으로 사용 가능한 장치 화면에 맞게 설정됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 62cbb3e6-e766-40a3-9c01-d22ade82b604
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 1%

---

# 기본 뷰어 영역{#main-viewer-area}

기본 보기 영역은 확대/축소 이미지와 견본이 차지하는 영역입니다. 크기를 지정하지 않은 경우 일반적으로 사용 가능한 장치 화면에 맞게 설정됩니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

임베디드 모드에서 작업할 때(기본 뷰어 영역에 명시적 크기가 지정된 경우) 뷰어는 단일 이미지로 작업 중인 견본 구성 요소의 높이만큼 기본 영역의 높이를 자동으로 감소하므로 견본이 필요하지 않습니다.

**기본 뷰어 영역의 CSS 속성**

다음 CSS 클래스 선택기를 사용하여 보기 영역의 모양이 제어됩니다.

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
   <td colname="col2"> <p>뷰어 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 16진수 형식의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 흰색 배경이 있는 뷰어 설정( `#FFFFFF`) 및 의 크기를 512 x 288 픽셀로 만듭니다.

```
.s7zoomviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
