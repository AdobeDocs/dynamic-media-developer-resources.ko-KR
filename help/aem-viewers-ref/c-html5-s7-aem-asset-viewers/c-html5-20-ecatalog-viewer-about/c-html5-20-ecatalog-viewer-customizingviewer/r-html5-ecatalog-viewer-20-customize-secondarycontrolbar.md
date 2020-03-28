---
description: 보조 컨트롤 막대는 첫 번째 및 마지막 페이지 단추가 포함된 사각형 영역과 CSS에서 사용할 수 있게 되면 페이지 표시기가 있습니다.
seo-description: 보조 컨트롤 막대는 첫 번째 및 마지막 페이지 단추가 포함된 사각형 영역과 CSS에서 사용할 수 있게 되면 페이지 표시기가 있습니다.
seo-title: 보조 컨트롤 막대
solution: Experience Manager
title: 보조 컨트롤 막대
topic: Dynamic media
uuid: 9a91da6b-0d9b-4b4c-9659-86a64e624947
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 보조 컨트롤 막대{#secondary-control-bar}

보조 컨트롤 막대는 첫 번째 및 마지막 페이지 단추가 포함된 사각형 영역과 CSS에서 사용할 수 있게 되면 페이지 표시기가 있습니다.

기본적으로 휴대폰에만 표시되며 뷰어 아래쪽에 있습니다. 항상 사용 가능한 전체 뷰어 너비를 사용합니다. 뷰어 컨테이너를 기준으로 색상, 높이 및 세로 위치를 CSS로 변경할 수 있습니다.

보조 컨트롤 막대의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

`.s7ecatalogviewer .s7secondarycontrols .s7controlbar`

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
   <td colname="col2"> <p>뷰어 맨 위에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p>뷰어 아래쪽에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>기본 컨트롤 막대의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>보조 컨트롤 막대의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 72픽셀이고 뷰어 컨테이너 아래쪽에 위치한 회색 보조 컨트롤 막대를 설정하려면

```
.s7ecatalogviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```

