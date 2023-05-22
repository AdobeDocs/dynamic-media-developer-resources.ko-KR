---
title: 페이지 표시기
description: 페이지 표시기에는 현재 페이지 인덱스 및 총 페이지 수가 표시됩니다. 데스크탑 시스템 및 태블릿의 주 제어 막대에 나타나며 휴대 전화에서는 보조 제어 막대에 추가됩니다. 페이지 표시기의 크기를 조정하고, 스킨을 지정하고, CSS로 위치를 지정할 수 있습니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 38241e96-ee7f-4dc1-a2a6-4a76e25b00dc
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 3%

---

# 페이지 표시기{#page-indicator}

페이지 표시기에는 현재 페이지 인덱스 및 총 페이지 수가 표시됩니다. 데스크탑 시스템 및 태블릿의 주 제어 막대에 나타나며 휴대 전화에서는 보조 제어 막대에 추가됩니다. 페이지 표시기의 크기를 조정하고, 스킨을 지정하고, CSS로 위치를 지정할 수 있습니다.

모양 페이지 표시기는 다음 CSS 클래스 선택기로 제어합니다.

`.s7ecatalogsearchviewer .s7pageindicator`

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
   <td colname="col2"> <p>패딩을 포함한 기본 컨트롤 막대(데스크탑 시스템 및 태블릿) 또는 보조 컨트롤 막대(휴대폰)의 위쪽 테두리에서 배치합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p>패딩을 포함한 기본 컨트롤 막대(데스크탑 시스템 및 태블릿) 또는 보조 컨트롤 막대(휴대폰)의 오른쪽 테두리에서 배치합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 왼쪽 </span> </p> </td> 
   <td colname="col2"> <p>패딩을 포함하여 기본 컨트롤 막대(데스크탑 시스템 및 태블릿) 또는 보조 컨트롤 막대(휴대폰)의 왼쪽 테두리에서 배치합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p>패딩을 포함하여 기본 컨트롤 막대(데스크탑 시스템 및 태블릿) 또는 보조 컨트롤 막대(휴대폰)의 아래쪽 테두리에서 배치합니다. </p> </td> 
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

예 - 기본 컨트롤 막대의 맨 아래에서 가로 가운데에 4픽셀씩 배치되어 있는 56 x 28픽셀 페이지 표시기를 설정하고 14픽셀 Helvetica® 글꼴을 사용합니다.

```
.s7ecatalogsearchviewer  .s7pageindicator { 
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
