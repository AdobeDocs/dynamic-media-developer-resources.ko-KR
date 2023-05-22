---
title: 검색 효과
description: 뷰어는 카탈로그에서 발견된 단어 또는 구를 강조 표시하기 위해 기본 보기 위에 검색 결과 영역을 표시합니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 3591edb0-4b0a-4761-af87-c372132c5138
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 1%

---

# 검색 효과{#search-effect}

뷰어는 카탈로그에서 발견된 단어 또는 구를 강조 표시하기 위해 기본 보기 위에 검색 결과 영역을 표시합니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

다음 CSS 클래스 선택기를 사용하여 검색 결과 영역의 모양이 제어됩니다.

`.s7ecatalogsearchviewer .s7searcheffect .s7region`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 </span> </p> </td> 
   <td colname="col2"> <p>검색 결과 영역의 배경입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 반투명 노란색 채우기로 검색 결과 영역을 설정하려면:

```
.s7ecatalogsearchviewer .s7searcheffect .s7region { 
 background: rgba(255,255,0, 0.5); 
}
```
