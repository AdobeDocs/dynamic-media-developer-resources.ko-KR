---
description: 텍스트 상자에서는 다음 문서 속성이 지원됩니다.
seo-description: 텍스트 상자에서는 다음 문서 속성이 지원됩니다.
seo-title: 문서(텍스트 상자) 속성
solution: Experience Manager
title: 문서(텍스트 상자) 속성
topic: Scene7 Image Serving - Image Rendering API
uuid: 743a773a-83b0-4667-9c67-4cefbfe77bbd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 1%

---


# 문서(텍스트 상자) 속성{#document-text-box-properties}

텍스트 상자에서는 다음 문서 속성이 지원됩니다.

<table id="table_8E1DF8E6BD894D7A9ACFC839918E2315"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>명령</b> </th> 
   <th class="entry"> <b>설명</b> </th> 
   <th class="entry"> <b>주의</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \fontbl  </span> </td> 
   <td> <p>글꼴 표. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fcharset  <span class="varname"> N  </span> </span> </td> 
   <td> <p>글꼴 <i>N</i>에 대한 문자 집합. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \colortbl  </span> </td> 
   <td> <p>RGB 색상표. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cmykcolortbl  </span> </td> 
   <td> <p>CMYK 색상표. </p> </td> 
   <td> <p>Scene7 확장 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \*\iscolortbl  </span> </td> 
   <td> <p>이미지 제공 색상에 대한 색상표입니다. </p> </td> 
   <td> <p>Scene7 확장;<span class="codeph"> textPs= </span>만 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \red  <span class="varname"> N  </span> </span> </td> 
   <td> <p>빨강 색상 구성 요소 </p> </td> 
   <td> <p><span class="codeph"> \colortbl </span>;에만 나타날 수 있습니다.0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \green  <span class="varname"> N  </span> </span> </td> 
   <td> <p>녹색 색상 구성 요소 </p> </td> 
   <td> <p><span class="codeph"> \colortbl </span>;에만 나타날 수 있습니다.0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \blue  <span class="varname"> N  </span> </span> </td> 
   <td> <p>파란색 구성 요소 </p> </td> 
   <td> <p><span class="codeph"> \colortbl </span>;에만 나타날 수 있습니다.0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cyan  <span class="varname"> N  </span> </span> </td> 
   <td> <p>청록 색상 구성 요소. </p> </td> 
   <td> <p>Scene7 확장;는 <span class="codeph"> \cmykcolortbl </span>;에만 표시됩니다.0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \magenta  <span class="varname"> N  </span> </span> </td> 
   <td> <p>자홍 색상 구성 요소. </p> </td> 
   <td> <p>Scene7 확장;는 <span class="codeph"> \cmykcolortbl </span>;에만 표시됩니다.0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \yellow  <span class="varname"> N  </span> </span> </td> 
   <td> <p>노란색 색상 구성 요소 </p> </td> 
   <td> <p>Scene7 확장;는 <span class="codeph"> \cmykcolortbl </span>;에만 표시됩니다.0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \black  <span class="varname"> N  </span> </span> </td> 
   <td> <p>검정 색상 구성 요소. </p> </td> 
   <td> <p>Scene7 확장;는 <span class="codeph"> \cmykcolortbl </span>;에만 표시됩니다.0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margl  <span class="varname"> N  </span> </span> </td> 
   <td> <p>왼쪽 여백입니다. </p> </td> 
   <td> <p>Twips;<span class="codeph"> textPs= </span>만 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margarr  <span class="varname"> N  </span> </span> </td> 
   <td> <p>오른쪽 여백. </p> </td> 
   <td> <p>Twips;<span class="codeph"> textPs= </span>만 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margart  <span class="varname"> N  </span> </span> </td> 
   <td> <p>위쪽 여백. </p> </td> 
   <td> <p>Twips;<span class="codeph"> textPs= </span>만 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margb  <span class="varname"> N  </span> </span> </td> 
   <td> <p>아래쪽 여백. </p> </td> 
   <td> <p>Twips;<span class="codeph"> textPs= </span>만 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalt  </span> </td> 
   <td> <p>텍스트 상자에서 텍스트를 맨 위로 정렬합니다. </p> </td> 
   <td> <p>기본값 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalb  </span> </td> 
   <td> <p>텍스트 상자의 텍스트를 아래에서 정렬하십시오. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertks  </span> </td> 
   <td> <p>텍스트 상자에 텍스트를 가운데로 정렬합니다. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \stextflow  <span class="varname"> N  </span> </span> </td> 
   <td> <p>텍스트 흐름 방향. </p> </td> 
   <td> <p>언어별 텍스트 흐름;<span class="codeph"> textPs= </span>만 0(기본값) 왼쪽-오른쪽, 위쪽-아래쪽(유럽) 1 위쪽-아래쪽, 오른쪽-왼쪽(극동) </p> </td> 
  </tr> 
 </tbody> 
</table>

