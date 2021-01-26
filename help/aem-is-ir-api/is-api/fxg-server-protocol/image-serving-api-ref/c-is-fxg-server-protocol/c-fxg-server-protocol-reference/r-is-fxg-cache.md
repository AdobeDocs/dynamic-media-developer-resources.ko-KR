---
description: 캐시 제어. 선택적으로 클라이언트측 캐싱(브라우저, 프록시 서버, 네트워크 캐싱 시스템)을 비활성화하고 내부 플랫폼 서버 캐시에서 캐싱을 수행할 수 있습니다.
seo-description: 캐시 제어. 선택적으로 클라이언트측 캐싱(브라우저, 프록시 서버, 네트워크 캐싱 시스템)을 비활성화하고 내부 플랫폼 서버 캐시에서 캐싱을 수행할 수 있습니다.
seo-title: 캐시
solution: Experience Manager
title: 캐시
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 10332f0d-4ed3-4981-8034-46dffa5d68b0
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# 캐시{#cache}

캐시 제어. 선택적으로 클라이언트측 캐싱(브라우저, 프록시 서버, 네트워크 캐싱 시스템)을 비활성화하고 내부 플랫폼 서버 캐시에서 캐싱을 수행할 수 있습니다.

`&cache= *`cacheControl`*`

`&cache= *``*, *`clientControlserverControl`*`

<table id="simpletable_DA4D92F0AEF84FD49953876796058B7F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> serverControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
</table>

*`cacheControl`* 값을 하나만 지정하면 클라이언트와 서버 캐시 모두에 적용됩니다.

요청 속성을 참조하십시오. 요청이 응답 이미지를 반환하지 않을 때 무시됩니다. *`clientControl`* 은 이미지 카탈로그에서 클라이언트측 캐싱을 비활성화하면 무시됩니다(음수 값이  `catalog::Expiration` 있는 경우).

기본값은 `cache=on,on`입니다.
