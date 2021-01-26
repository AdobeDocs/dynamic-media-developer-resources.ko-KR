---
description: 문자를 인코딩하려면 다음 명령을 사용합니다.
seo-description: 문자를 인코딩하려면 다음 명령을 사용합니다.
seo-title: 문자 인코딩
solution: Experience Manager
title: 문자 인코딩
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 7b19b831-b40c-4f26-83a4-732c578dbbf0
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 2%

---


# 문자 인코딩{#character-encoding}

문자를 인코딩하려면 다음 명령을 사용합니다.

<table id="table_EB0C1B674BEA4A37964FB4BF559E0005"> 
 <thead> 
  <tr> 
   <th class="entry"> 명령 </th> 
   <th class="entry"> 설명 </th> 
   <th class="entry"> 주의 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph">\'<span class="varname"> HH</span></span> </td> 
   <td> <p>8비트 단일 문자입니다. </p> </td> 
   <td> <p><span class="varname"> 2</span> 자리 16진수 값이어야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\<span class="varname"> uN</span></span> </td> 
   <td> <p>단일 유니코드 문자. </p> </td> 
   <td> <p><span class="varname"> 부호 </span> 있는 2바이트 정수로 32767보다 큰 유니코드 값은 음수로 표시되어야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\<span class="varname"> ucN</span></span> </td> 
   <td> <p>유니코드 문자 크기. </p> </td> 
   <td> <p>주어진 유니코드 문자에 해당하는 바이트 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch  </span> </td> 
   <td> <p>낮은 ANSI 영역의 문자 다음에 나옵니다. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \hich  </span> </td> 
   <td> <p>높은 ANSI 영역의 문자 다음에 나옵니다. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch  </span> </td> 
   <td> <p>더블바이트 문자는 뒤에 옵니다. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

