---
title: 문자 인코딩
description: 문자 인코딩에 다음 명령을 사용합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a03f08f7-e9cc-458f-9ff0-7721f1dbc4cc
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 2%

---

# 문자 인코딩{#character-encoding}

문자 인코딩에 다음 명령을 사용합니다.

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
   <td> <p>단일 8비트 문자 </p> </td> 
   <td> <p><span class="varname"> HH</span> 2자리 16진수 값이어야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\u<span class="varname"> N</span></span> </td> 
   <td> <p>단일 유니코드 문자 </p> </td> 
   <td> <p><span class="varname"> N</span> 는 부호 있는 2바이트 정수이므로 32767보다 큰 유니코드 값은 음수로 표현해야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\uc<span class="varname"> N</span></span> </td> 
   <td> <p>유니코드 문자 크기입니다. </p> </td> 
   <td> <p>지정된 유니코드 문자에 해당하는 바이트 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch </span> </td> 
   <td> <p>낮은 ANSI 영역의 문자입니다. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \which </span> </td> 
   <td> <p>높은 ANSI 영역의 문자입니다. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch </span> </td> 
   <td> <p>2바이트 문자가 뒤에 옵니다. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>
