---
description: 텍스트 서식을 지정할 때 다음 특수 엔티티를 사용합니다.
solution: Experience Manager
title: 특수 텍스트 엔티티
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3798dd83-897a-441c-a7c4-ef7325b20f16
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 4%

---

# 특수 텍스트 엔티티{#special-text-entities}

텍스트 서식을 지정할 때 다음 특수 엔티티를 사용합니다.

<table id="table_CFEB845C1B9A475CA52ECDFA9BB59A9D"> 
 <thead> 
  <tr> 
   <th class="entry"> 명령 </th> 
   <th class="entry"> 설명 </th> 
   <th class="entry"> 주의 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \par</span> </td> 
   <td> <p>단락 나누기. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \라인 </span> </td> 
   <td> <p>줄바꿈. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \\ </span> </td> 
   <td> <p>슬래시. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> &amp;lbrace;  </span> </td> 
   <td> <p>중괄호. </p> </td> 
   <td> <p>중괄호는 HTTP로 인코딩되어야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> &amp;rbrace;  </span> </td> 
   <td> <p>중괄호. </p> </td> 
   <td> <p>중괄호는 HTTP로 인코딩되어야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \~ </span> </td> 
   <td> <p>끊김 없는 공백. </p> </td> 
   <td> <p><span class="codeph"> textPs=</span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \_</span> </td> 
   <td> <p>줄바꿈 없는 하이픈. </p> </td> 
   <td> <p><span class="codeph"> textPs=</span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \- </span> </td> 
   <td> <p>하이픈 옵션. </p> </td> 
   <td> <p><span class="codeph"> textPs=</span> only. </p> </td> 
  </tr> 
 </tbody> 
</table>
