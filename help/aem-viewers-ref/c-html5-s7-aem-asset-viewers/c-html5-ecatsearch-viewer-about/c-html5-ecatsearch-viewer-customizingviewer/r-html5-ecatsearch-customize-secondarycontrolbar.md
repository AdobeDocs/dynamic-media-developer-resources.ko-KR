---
description: 보조 컨트롤 막대는 [첫 번째 페이지] 및 [마지막 페이지] 단추가 포함된 사각형 영역과 CSS로 사용할 수 있도록 만든 경우 [페이지 표시기]입니다.
seo-description: 보조 컨트롤 막대는 [첫 번째 페이지] 및 [마지막 페이지] 단추가 포함된 사각형 영역과 CSS로 사용할 수 있도록 만든 경우 [페이지 표시기]입니다.
seo-title: 보조 컨트롤 막대
solution: Experience Manager
title: 보조 컨트롤 막대
topic: Dynamic media
uuid: 38217d2a-8668-46e1-9df1-f29c1c7e0798
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 2%

---


# 보조 컨트롤 막대{#secondary-control-bar}

보조 컨트롤 막대는 [첫 번째 페이지] 및 [마지막 페이지] 단추가 포함된 사각형 영역과 CSS로 사용할 수 있도록 만든 경우 [페이지 표시기]입니다.

기본적으로 휴대폰에만 표시되며 뷰어 아래쪽에 있습니다. 항상 사용 가능한 전체 뷰어 너비를 사용합니다. 뷰어 컨테이너를 기준으로 색상, 높이 및 세로 위치를 CSS로 변경할 수 있습니다.

보조 컨트롤 막대의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

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
   <td colname="col1"> <p> <span class="codeph"> 최상위 </span> </p> </td> 
   <td colname="col2"> <p>뷰어 상단에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p>뷰어 아래쪽의 위치입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>기본 컨트롤 막대의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>보조 컨트롤 막대의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 72픽셀이고 뷰어 컨테이너의 아래쪽에 위치한 회색 보조 컨트롤 막대를 설정하려면

```
.s7ecatalogsearchviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```

