---
description: 페이지 표시기에는 현재 페이지 색인과 총 페이지 수가 표시됩니다. 데스크톱 시스템 및 태블릿의 주 컨트롤 막대에 표시되고 휴대폰에서는 보조 컨트롤 막대에 추가됩니다. 페이지 표시기는 CSS로 크기 조정, 스킨 및 배치할 수 있습니다.
seo-description: 페이지 표시기에는 현재 페이지 색인과 총 페이지 수가 표시됩니다. 데스크톱 시스템 및 태블릿의 주 컨트롤 막대에 표시되고 휴대폰에서는 보조 컨트롤 막대에 추가됩니다. 페이지 표시기는 CSS로 크기 조정, 스킨 및 배치할 수 있습니다.
seo-title: 페이지 표시기
solution: Experience Manager
title: 페이지 표시기
topic: Dynamic media
uuid: 5e33c149-fdc7-419a-b5ff-b9be3f342d9f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 페이지 표시기{#page-indicator}

페이지 표시기에는 현재 페이지 색인과 총 페이지 수가 표시됩니다. 데스크톱 시스템 및 태블릿의 주 컨트롤 막대에 표시되고 휴대폰에서는 보조 컨트롤 막대에 추가됩니다. 페이지 표시기는 CSS로 크기 조정, 스킨 및 배치할 수 있습니다.

페이지 표시기의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

`.s7ecatalogviewer .s7pageindicator`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최상위 </span> </p> </td> 
   <td colname="col2"> <p>기본 컨트롤 막대(데스크톱 시스템 및 태블릿에 있음) 또는 보조 컨트롤 막대(휴대폰)의 위쪽 테두리에서 패딩 등 위치를 지정할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p>기본 컨트롤 막대(데스크톱 시스템 및 태블릿에 있음) 또는 보조 컨트롤 막대(휴대폰)의 오른쪽 테두리에서 패딩 등 위치를 지정할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 왼쪽 </span> </p> </td> 
   <td colname="col2"> <p>기본 컨트롤 막대(데스크톱 시스템 및 태블릿에 있음) 또는 보조 컨트롤 막대(휴대폰)의 왼쪽 테두리에서 패딩 등의 위치를 지정할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p>기본 컨트롤 막대(데스크톱 시스템 및 태블릿에서) 또는 보조 컨트롤 막대(휴대폰)의 아래쪽 테두리에서 패딩 등 위치를 지정할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>페이지 표시기의 너비입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>페이지 표시기의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>글꼴 색상. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>글꼴 이름. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 크기 </span> </p> </td> 
   <td colname="col2"> <p>글꼴 크기. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 56 x 28픽셀의 페이지 표시기를 기본 컨트롤 막대 아래쪽에서 가로로 가운데에 정렬하고 4픽셀의 위치를 지정하고 14픽셀의 Helvetica 글꼴을 사용하려면

```
.s7ecatalogviewer  .s7pageindicator { 
 position:absolute; 
 bottom: 4px; 
 margin-left: -28px;  
 left: 50%; 
 width:56px; 
 height:28px; 
 font-family: Helvetica; 
 font-size:14px; 
}
```

