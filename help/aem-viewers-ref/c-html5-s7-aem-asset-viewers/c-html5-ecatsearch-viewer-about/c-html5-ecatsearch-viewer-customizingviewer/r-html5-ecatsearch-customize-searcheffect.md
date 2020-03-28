---
description: 뷰어는 기본 보기 위에 검색 결과 영역을 표시하여 카탈로그에 있는 단어나 구문을 강조 표시합니다.
seo-description: 뷰어는 기본 보기 위에 검색 결과 영역을 표시하여 카탈로그에 있는 단어나 구문을 강조 표시합니다.
seo-title: 검색 효과
solution: Experience Manager
title: 검색 효과
topic: Dynamic media
uuid: 3a076ff8-2da5-4020-8a77-8f5a256afefe
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# 검색 효과{#search-effect}

뷰어는 기본 보기 위에 검색 결과 영역을 표시하여 카탈로그에 있는 단어나 구문을 강조 표시합니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

검색 결과 영역의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

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

예 - 반투명 노란색 채우기로 검색 결과 영역을 설정하려면

```
.s7ecatalogsearchviewer .s7searcheffect .s7region { 
 background: rgba(255,255,0, 0.5); 
}
```

