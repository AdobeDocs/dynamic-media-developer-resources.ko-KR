---
description: 캐시 컨트롤을 참조하십시오. 선택적으로 클라이언트측 캐싱(브라우저, 프록시 서버, 네트워크 캐싱 시스템)을 비활성화하고 내부 플랫폼 서버 캐시에서 캐싱을 수행할 수 있습니다.
seo-description: 캐시 컨트롤을 참조하십시오. 선택적으로 클라이언트측 캐싱(브라우저, 프록시 서버, 네트워크 캐싱 시스템)을 비활성화하고 내부 플랫폼 서버 캐시에서 캐싱을 수행할 수 있습니다.
seo-title: 캐시
solution: Experience Manager
title: 캐시
topic: Scene7 Image Serving - Image Rendering API
uuid: 08f4e4d0-0f7d-48fe-956c-284af97c902e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 1%

---


# 캐시{#cache}

캐시 컨트롤을 참조하십시오. 선택적으로 클라이언트측 캐싱(브라우저, 프록시 서버, 네트워크 캐싱 시스템)을 비활성화하고 내부 플랫폼 서버 캐시에서 캐싱을 수행할 수 있습니다.

`cache= *`cacheControl`*`

`cache= *``*, *`clientControlserverControl`*`

<table id="simpletable_70ACECAEA02F400C83B598FA13F1D00B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> on|off|validate|update</span> </p> </td> 
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

` *`cacheControl`*` 값을 하나만 지정하면 클라이언트와 서버 캐시 모두에 적용됩니다.

`validate` 키워드를 사용하면 캐시 항목이 자동으로 만료될 때까지 기다릴 필요 없이 이미지 파일이 변경된 후 캐시 항목을 업데이트할 수 있습니다. 클라이언트 캐싱은 이 명령의 영향을 받지 않습니다.

`update` 키워드를 사용하여 서버측 캐시 항목을 강제로 업데이트할 수 있습니다. 이 기능은 파일 이름 또는 관련 글꼴 ID를 변경하지 않고 글꼴 파일을 수정하는 경우와 같이 캐시 유효성 검사 메커니즘에 의해 직접 추적되지 않는 리소스가 변경된 후에 유용합니다.

중첩 요청에 지정된 경우, `cache=on`은 중첩된 요청에 의해 생성된 이미지의 서버측 지속적인 캐싱을 활성화합니다. 동일한 매개 변수를 사용하여 동일한 중첩 요청을 반복적으로 호출해야 하는 경우에만 중첩된 요청에 대해 캐싱을 활성화하는 것이 좋습니다.

## 속성 {#section-dfd0b2f92b3743fc8b9d2c35a786eb81}

요청 속성을 참조하십시오. 현재 레이어 설정에 관계없이 적용됩니다. 요청이 응답 이미지를 반환하지 않을 때 무시됩니다. *`clientControl`*는 이미지 카탈로그에서 클라이언트측 캐싱을 비활성화하면 무시됩니다(`catalog::Expiration`에 음수 값이 있는 경우).

클라이언트측 캐시 컨트롤( `on` 및 `off` 전용)도 [!DNL /is/content/]의 정적 컨텐츠 요청에 사용할 수 있습니다.

## 기본값 {#section-4124b2c836e2491489b9009a92fe4f22}

`cache=on,on` HTTP 요청에 대해, 중첩된/ `cache=off` 포함된 요청에 대해, 정적 컨텐츠 요청 `cache=on` 에 대해 설명합니다.

## 참조 {#section-7c2ac171fa0e4aa4a2e9955fd2d2013e}

[카탈로그::만료](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
