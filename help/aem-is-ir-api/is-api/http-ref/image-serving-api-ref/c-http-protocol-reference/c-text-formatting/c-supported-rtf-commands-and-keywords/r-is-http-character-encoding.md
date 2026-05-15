---
title: 문자 인코딩
description: 문자 인코딩에 다음 명령을 사용합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a03f08f7-e9cc-458f-9ff0-7721f1dbc4cc
TQID: 'https://experienceleague.adobe.com/rptRmm7xxUUF2l5WTYXjvbaifW2z5XKeCQIqa5XLFh4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 94
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
   <td> <p><span class="varname"> HH</span>은(는) 2자리 16진수 값이어야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\u<span class="varname"> N</span></span> </td> 
   <td> <p>단일 유니코드 문자 </p> </td> 
   <td> <p><span class="varname"> N</span>은(는) 부호 있는 2바이트 정수이므로 32767보다 큰 유니코드 값은 음수로 표현해야 합니다. </p> </td> 
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
