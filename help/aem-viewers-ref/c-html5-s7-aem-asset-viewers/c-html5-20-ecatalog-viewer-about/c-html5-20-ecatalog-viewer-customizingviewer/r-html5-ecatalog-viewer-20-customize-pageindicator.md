---
title: 페이지 표시기
description: 페이지 표시기에는 현재 페이지 색인과 총 페이지 수가 표시됩니다. 데스크톱 시스템 및 태블릿의 기본 컨트롤 모음에 표시되고 휴대 전화에서는 보조 컨트롤 모음에 추가됩니다. 페이지 표시기의 크기는 CSS로 지정하고, 스킨을 지정하고, 배치할 수 있습니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: c63af583-274c-4052-8186-604119a368af
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 3%

---

# 페이지 표시기{#page-indicator}

페이지 표시기에는 현재 페이지 색인과 총 페이지 수가 표시됩니다. 데스크톱 시스템 및 태블릿의 기본 컨트롤 모음에 표시되고 휴대 전화에서는 보조 컨트롤 모음에 추가됩니다. 페이지 표시기의 크기는 CSS로 지정하고, 스킨을 지정하고, 배치할 수 있습니다.

페이지 표시기의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

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
   <td colname="col2"> <p>기본 컨트롤 막대(데스크톱 시스템 및 태블릿의 경우) 또는 보조 컨트롤 막대(휴대폰의 경우)의 위쪽 테두리에서 패딩을 배치합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p>기본 컨트롤 막대(데스크톱 시스템 및 태블릿의 경우) 또는 보조 컨트롤 막대(휴대폰의 경우)의 오른쪽 테두리에서 패딩을 배치합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 왼쪽 </span> </p> </td> 
   <td colname="col2"> <p>기본 컨트롤 막대(데스크톱 시스템 및 태블릿의 경우) 또는 보조 컨트롤 막대(휴대폰의 경우)(패딩 포함)의 왼쪽 테두리에서 배치합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p>기본 컨트롤 막대(데스크톱 시스템 및 태블릿의 경우) 또는 보조 컨트롤 막대(휴대폰의 경우)의 안쪽 테두리에서 패딩을 배치합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>페이지 표시기의 폭입니다. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>글꼴 크기입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 56 x 28픽셀인 페이지 표시기를 가로 방향으로 가운데 맞춤하고 기본 컨트롤 막대의 하단에서 4픽셀을 배치하여 14픽셀 Helvetica® 글꼴을 사용합니다.

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
