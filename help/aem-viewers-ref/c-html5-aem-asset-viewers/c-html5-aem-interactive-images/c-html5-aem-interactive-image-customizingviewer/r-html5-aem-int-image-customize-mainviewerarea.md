---
description: 기본 보기 영역은 확대/축소 이미지가 차지하는 영역입니다. 크기가 지정되지 않은 경우 일반적으로 사용 가능한 장치 화면에 맞도록 설정됩니다.
solution: Experience Manager
title: 기본 뷰어 영역
feature: Dynamic Media Classic,Viewers,SDK/API,대화형 이미지
role: Developer,Business Practitioner
exl-id: c8005e7e-dff6-4f40-a94c-6fb6640e827f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---

# 기본 뷰어 영역{#main-viewer-area}

기본 보기 영역은 확대/축소 이미지가 차지하는 영역입니다. 크기가 지정되지 않은 경우 일반적으로 사용 가능한 장치 화면에 맞도록 설정됩니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

보기 영역의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7interactiveimage
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

예 - 흰색 배경( `#FFFFFF`)을 사용하여 뷰어를 설정하고 크기를 1174 x 500픽셀로 만듭니다.

```
.s7interactiveimage { 
 background-color: #FFFFFF; 
 width: 1174px; 
 height: 500px;  
}
```
