---
title: 기본 뷰어 영역
description: 메인 뷰 영역은 스핀 이미지가 차지하는 영역입니다. 크기를 지정하지 않은 경우 일반적으로 사용 가능한 장치 화면에 맞게 설정됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 6cd9c375-8890-4033-b187-b95b26dd6009
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# 기본 뷰어 영역{#main-viewer-area}

메인 뷰 영역은 스핀 이미지가 차지하는 영역입니다. 크기를 지정하지 않은 경우 일반적으로 사용 가능한 장치 화면에 맞게 설정됩니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

다음 CSS 클래스 선택기를 사용하여 보기 영역의 모양이 제어됩니다.

```
.s7spinviewer
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
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>뷰어의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>뷰어 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p> 16진수 형식의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 흰색 배경(`#FFFFFF`)을 가진 뷰어를 설정하고 크기를 512 x 288픽셀로 지정합니다.

```
.s7spinviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
