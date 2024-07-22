---
title: 보조 컨트롤 막대
description: 보조 컨트롤 막대는 CSS에서 사용할 수 있을 때 첫 번째 및 마지막 페이지 단추와 페이지 표시기가 포함된 사각형 영역입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e5d6abe8-0ae9-4ccd-b311-5895e09310b2
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# 보조 컨트롤 막대{#secondary-control-bar}

보조 컨트롤 막대는 CSS에서 사용할 수 있을 때 첫 번째 및 마지막 페이지 단추와 페이지 표시기가 포함된 사각형 영역입니다.

기본적으로 휴대폰에만 표시되고, 뷰어 아래쪽에 있습니다. 항상 사용 가능한 전체 뷰어 너비를 사용합니다. 뷰어 컨테이너를 기준으로 CSS별로 색상, 높이 및 세로 위치를 변경할 수 있습니다.

보조 컨트롤 막대의 모양은 다음 CSS 클래스 선택기를 사용하여 제어됩니다.

`.s7ecatalogsearchviewer .s7secondarycontrols .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 상위 </span> </p> </td> 
   <td colname="col2"> <p>뷰어의 맨 위에 있는 위치입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p>뷰어 아래에서 위치 지정. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>기본 컨트롤 막대의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p>보조 컨트롤 막대의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 뷰어 컨테이너의 맨 아래에 위치하며 높이가 72픽셀인 회색 보조 컨트롤 막대를 설정합니다.

```
.s7ecatalogsearchviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```
