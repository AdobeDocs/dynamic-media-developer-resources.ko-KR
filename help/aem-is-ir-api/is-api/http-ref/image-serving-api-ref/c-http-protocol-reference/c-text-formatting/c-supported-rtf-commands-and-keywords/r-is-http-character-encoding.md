---
description: 문자를 인코딩하려면 다음 명령을 사용합니다.
seo-description: 문자를 인코딩하려면 다음 명령을 사용합니다.
seo-title: 문자 인코딩
solution: Experience Manager
title: 문자 인코딩
topic: Scene7 Image Serving - Image Rendering API
uuid: 7b19b831-b40c-4f26-83a4-732c578dbbf0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Character encoding{#character-encoding}

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
   <td> <p>8비트 단일 문자 </p> </td> 
   <td> <p><span class="varname"> HH는</span> 2자리 16진수 값이어야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\u<span class="varname"> N</span></span> </td> 
   <td> <p>단일 유니코드 문자. </p> </td> 
   <td> <p><span class="varname"> N은</span> 부호 있는 2바이트 정수이므로 32767보다 큰 유니코드 값은 음수로 표시되어야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\uc<span class="varname"> N</span></span> </td> 
   <td> <p>유니코드 문자 크기. </p> </td> 
   <td> <p>주어진 유니코드 문자에 해당하는 바이트 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch </span> </td> 
   <td> <p>낮은 ANSI 영역의 문자 뒤에 오는 경우 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \hich </span> </td> 
   <td> <p>높은 ANSI 영역의 문자 뒤에 옵니다. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch </span> </td> 
   <td> <p>2바이트 문자 다음에 나옵니다. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

