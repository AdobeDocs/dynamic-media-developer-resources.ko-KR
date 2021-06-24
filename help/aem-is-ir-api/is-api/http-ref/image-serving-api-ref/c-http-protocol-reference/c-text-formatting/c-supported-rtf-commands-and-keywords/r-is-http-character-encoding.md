---
description: 문자를 인코딩하려면 다음 명령을 사용하십시오.
solution: Experience Manager
title: 문자 인코딩
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: a03f08f7-e9cc-458f-9ff0-7721f1dbc4cc
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 2%

---

# 문자 인코딩{#character-encoding}

문자를 인코딩하려면 다음 명령을 사용하십시오.

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
   <td> <p><span class="varname"> </span> 는 2자리 16진수 값이어야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\<span class="varname"> uN</span></span> </td> 
   <td> <p>단일 유니코드 문자입니다. </p> </td> 
   <td> <p><span class="varname"> </span> 서명된 2바이트 정수를 사용하므로 32767보다 큰 유니코드 값은 음수로 표현해야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\<span class="varname"> ucN</span></span> </td> 
   <td> <p>유니코드 문자 크기입니다. </p> </td> 
   <td> <p>지정된 유니코드 문자를 해당하는 바이트 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch  </span> </td> 
   <td> <p>낮은 ANSI 영역의 문자가 따릅니다. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \h  </span> </td> 
   <td> <p>높은 ANSI 영역의 문자가 따릅니다. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch  </span> </td> 
   <td> <p>더블바이트 문자는 다음에 옵니다. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>
