---
description: 텍스트 상자에서는 다음 문서 속성이 지원됩니다.
solution: Experience Manager
title: 문서(텍스트 상자) 속성
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e9d21a39-4d98-4115-8179-ab5acf713c80
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '214'
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
   <td> <span class="codeph"> \fonttbl  </span> </td> 
   <td> <p>글꼴 테이블입니다. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fcharset  <span class="varname"> N  </span> </span> </td> 
   <td> <p>글꼴 <i>N</i>에 대해 설정된 문자. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \colortbl  </span> </td> 
   <td> <p>RGB 색상표. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cmykcolortbl  </span> </td> 
   <td> <p>CMYK 색상표 </p> </td> 
   <td> <p>Dynamic Media 확장. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \*\iscolortbl  </span> </td> 
   <td> <p>이미지 제공 색상의 색상 테이블입니다. </p> </td> 
   <td> <p>Dynamic Media 확장 <span class="codeph"> textPs= </span> 만 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \red  <span class="varname"> N  </span> </span> </td> 
   <td> <p>빨강 색상 구성 요소입니다. </p> </td> 
   <td> <p><span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \녹색  <span class="varname"> N  </span> </span> </td> 
   <td> <p>녹색 색상 구성 요소입니다. </p> </td> 
   <td> <p><span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \blue  <span class="varname"> N  </span> </span> </td> 
   <td> <p>파란색 구성 요소입니다. </p> </td> 
   <td> <p><span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cyan  <span class="varname"> N  </span> </span> </td> 
   <td> <p>시안 색상 구성 요소입니다. </p> </td> 
   <td> <p>Dynamic Media 확장 <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \magenta  <span class="varname"> N  </span> </span> </td> 
   <td> <p>자홍색 구성 요소입니다. </p> </td> 
   <td> <p>Dynamic Media 확장 <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \노란색  <span class="varname"> N  </span> </span> </td> 
   <td> <p>노란색 색상 구성 요소입니다. </p> </td> 
   <td> <p>Dynamic Media 확장 <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \black  <span class="varname"> N  </span> </span> </td> 
   <td> <p>검정색 구성 요소입니다. </p> </td> 
   <td> <p>Dynamic Media 확장 <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margl  <span class="varname"> N  </span> </span> </td> 
   <td> <p>왼쪽 여백. </p> </td> 
   <td> <p>트위프; <span class="codeph"> textPs= </span> 만 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margarr  <span class="varname"> N  </span> </span> </td> 
   <td> <p>오른쪽 여백. </p> </td> 
   <td> <p>트위프; <span class="codeph"> textPs= </span> 만 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margart  <span class="varname"> N  </span> </span> </td> 
   <td> <p>위쪽 여백. </p> </td> 
   <td> <p>트위프; <span class="codeph"> textPs= </span> 만 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margb  <span class="varname"> N  </span> </span> </td> 
   <td> <p>아래 여백. </p> </td> 
   <td> <p>트위프; <span class="codeph"> textPs= </span> 만 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalt  </span> </td> 
   <td> <p>텍스트 상자의 텍스트 위쪽 정렬. </p> </td> 
   <td> <p>기본값 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalb  </span> </td> 
   <td> <p>텍스트 상자의 텍스트를 아래쪽 정렬합니다. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \verbluk  </span> </td> 
   <td> <p>텍스트 상자에 텍스트를 가운데로 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \stextflow  <span class="varname"> N  </span> </span> </td> 
   <td> <p>텍스트 흐름 방향. </p> </td> 
   <td> <p>언어별 텍스트 흐름 <span class="codeph"> textPs= </span>만 0(기본값) 왼쪽, 오른쪽, 위쪽(유럽) 1 맨 아래, 오른쪽(극동) </p> </td> 
  </tr> 
 </tbody> 
</table>
