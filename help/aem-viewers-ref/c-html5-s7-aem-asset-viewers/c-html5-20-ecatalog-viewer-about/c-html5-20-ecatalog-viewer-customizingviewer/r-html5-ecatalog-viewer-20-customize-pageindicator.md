---
description: 페이지 표시기에는 현재 페이지 색인과 총 페이지 카운트가 표시됩니다. 데스크톱 시스템 및 태블릿의 주 컨트롤 막대에 표시되고 휴대 전화에서는 보조 컨트롤 막대에 추가됩니다. 페이지 표시기는 CSS로 크기 조정, 스킨 및 배치할 수 있습니다.
solution: Experience Manager
title: 페이지 표시기
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 3%

---


# 페이지 표시기{#page-indicator}

페이지 표시기에는 현재 페이지 색인과 총 페이지 카운트가 표시됩니다. 데스크톱 시스템 및 태블릿의 주 컨트롤 막대에 표시되고 휴대 전화에서는 보조 컨트롤 막대에 추가됩니다. 페이지 표시기는 CSS로 크기 조정, 스킨 및 배치할 수 있습니다.

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
   <td colname="col2"> <p>패딩을 포함하여 기본 컨트롤 막대(데스크톱 시스템 및 태블릿의 경우) 또는 보조 컨트롤 막대(휴대 전화의 경우)의 위쪽 테두리에서 배치합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p>패딩을 포함하여 기본 컨트롤 막대(데스크톱 시스템 및 태블릿의 경우) 또는 보조 컨트롤 막대(휴대 전화의 경우)의 오른쪽 테두리에서 배치합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 왼쪽 </span> </p> </td> 
   <td colname="col2"> <p>패딩을 포함하여 기본 컨트롤 막대(데스크톱 시스템 및 태블릿의 경우) 또는 보조 컨트롤 막대(휴대 전화의 경우)의 왼쪽 테두리에서 배치합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p>패딩을 포함하여 기본 컨트롤 막대(데스크톱 시스템 및 태블릿의 경우) 또는 보조 컨트롤 막대(휴대 전화의 경우)의 아래쪽 테두리에서 배치합니다. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>글꼴 이름. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 크기  </span> </p> </td> 
   <td colname="col2"> <p>글꼴 크기. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 56 x 28픽셀인 페이지 표시기를 기본 컨트롤 모음 아래쪽에서 가로로 가운데에 정렬하고 4픽셀을 배치하여 14픽셀의 Helvetica 글꼴을 사용하려면

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

