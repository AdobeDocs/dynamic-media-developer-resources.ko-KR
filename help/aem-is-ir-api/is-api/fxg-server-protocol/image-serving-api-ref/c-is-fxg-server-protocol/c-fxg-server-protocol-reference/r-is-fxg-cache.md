---
description: 캐시 제어. 클라이언트측 캐싱(브라우저, 프록시 서버, 네트워크 캐싱 시스템)을 선택적으로 비활성화하고 내부 플랫폼 서버 캐시에서 캐싱을 수행할 수 있습니다.
seo-description: 캐시 제어. 클라이언트측 캐싱(브라우저, 프록시 서버, 네트워크 캐싱 시스템)을 선택적으로 비활성화하고 내부 플랫폼 서버 캐시에서 캐싱을 수행할 수 있습니다.
seo-title: 캐시
solution: Experience Manager
title: 캐시
topic: Scene7 Image Serving - Image Rendering API
uuid: 10332f0d-4ed3-4981-8034-46dffa5d68b0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# cache{#cache}

캐시 제어. 클라이언트측 캐싱(브라우저, 프록시 서버, 네트워크 캐싱 시스템)을 선택적으로 비활성화하고 내부 플랫폼 서버 캐시에서 캐싱을 수행할 수 있습니다.

`&cache= *`cacheControl`*`

`&cache= *``*, *`clientControlserverControl`*`

<table id="simpletable_DA4D92F0AEF84FD49953876796058B7F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> cache <span class="varname"> Control</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> client <span class="varname"> Control</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> server <span class="varname"> Control</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
</table>

하나의 *`cacheControl`* 값만 지정하면 클라이언트와 서버 캐시 모두에 적용됩니다.

요청 속성입니다. 요청이 회신 이미지를 반환하지 않을 때 무시됩니다. *`clientControl`* 은 이미지 카탈로그에서 클라이언트측 캐싱을 비활성화하면 무시됩니다(음수 값이 있는 경우 `catalog::Expiration` ).

기본값은 `cache=on,on`입니다.
