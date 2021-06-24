---
description: 기본 보기 영역은 확대/축소 이미지와 색상 견본이 차지하는 영역입니다. 일반적으로 크기가 지정되지 않은 경우 사용 가능한 장치 화면에 맞게 설정됩니다.
solution: Experience Manager
title: 기본 뷰어 영역
feature: Dynamic Media Classic,Viewers,SDK/API,확대/축소
role: Developer,Business Practitioner
exl-id: 62cbb3e6-e766-40a3-9c01-d22ade82b604
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 1%

---

# 기본 뷰어 영역{#main-viewer-area}

기본 보기 영역은 확대/축소 이미지와 색상 견본이 차지하는 영역입니다. 일반적으로 크기가 지정되지 않은 경우 사용 가능한 장치 화면에 맞게 설정됩니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

내장 모드에서 작업할 때(기본 뷰어 영역에 명시적 크기가 주어질 때) 뷰어는 단일 이미지로 작업하는 [색상 견본] 구성 요소의 높이로 기본 영역의 높이를 자동으로 감소하므로 색상 견본이 필요하지 않습니다.

**기본 뷰어 영역의 CSS 속성**

보기 영역의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

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
   <td colname="col1"> <p> <span class="codeph"> 배경색  </span> </p> </td> 
   <td colname="col2"> <p> 16진수 형식의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 흰색 배경인 뷰어를 설정하고 크기를 512 x 288픽셀로 만들려면`#FFFFFF`

```
.s7zoomviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
