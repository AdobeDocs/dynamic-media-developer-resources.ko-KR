---
description: 캐시 제어. 클라이언트 측 캐싱(브라우저, 프록시 서버, 네트워크 캐싱 시스템)과 내부 캐싱을 선택적으로 비활성화할 수 있습니다. [!DNL Platform Server] 캐시.
solution: Experience Manager
title: 캐시
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 622c36fa-c209-4149-a7db-85067215b5e5
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---

# 캐시{#cache}

캐시 제어. 클라이언트 측 캐싱(브라우저, 프록시 서버, 네트워크 캐싱 시스템)과 내부 캐싱을 선택적으로 비활성화할 수 있습니다. [!DNL Platform Server] 캐시.

`&cache= *`cacheControl`*`

`&cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_DA4D92F0AEF84FD49953876796058B7F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 설정|해제</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 설정|해제</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> serverControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 설정|해제</span> </p></td> 
 </tr> 
</table>

하나만 *`cacheControl`* 값을 지정하면 클라이언트와 서버 캐시에 모두 적용됩니다.

요청 속성입니다. 요청이 회신 이미지를 반환하지 않을 때 무시됩니다. *`clientControl`* 이미지 카탈로그에서 클라이언트측 캐싱이 비활성화될 경우 가 무시됩니다 `catalog::Expiration` 에는 음수 값이 있습니다.)

기본값은 입니다. `cache=on,on`.
