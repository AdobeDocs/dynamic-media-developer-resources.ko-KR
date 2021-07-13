---
description: 클라이언트 메시지. 클라이언트가 서버 로그에 짧은 텍스트 메시지를 삽입할 수 있는 메커니즘을 제공합니다.
solution: Experience Manager
title: 메시지
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 47e51181-714c-4b25-a375-f3b2238cd534
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 7%

---

# 메시지{#message}

클라이언트 메시지. 클라이언트가 서버 로그에 짧은 텍스트 메시지를 삽입할 수 있는 메커니즘을 제공합니다.

`req=message&message= *`문자열`*`

<table id="simpletable_9AF29AA336C4447BBC2FD4A7D43ED91B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 문자열</span> </p> </td> 
  <td class="stentry"> <p>메시지 문자열입니다. </p></td> 
 </tr> 
</table>

HTTP 응답을 캐시할 수 없습니다. MIME 유형 `text/plain`으로 빈 응답이 반환됩니다.
