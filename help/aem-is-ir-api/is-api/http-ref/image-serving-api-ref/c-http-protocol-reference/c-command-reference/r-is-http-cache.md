---
description: 캐시 제어. 클라이언트 측 캐싱(브라우저, 프록시 서버, 네트워크 캐싱 시스템)과 내부 캐싱을 선택적으로 비활성화할 수 있습니다. [!DNL Platform Server] 캐시.
solution: Experience Manager
title: 캐시
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b631836-e5a8-4a56-a09a-35bb2474cc84
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 1%

---

# 캐시{#cache}

캐시 제어. 클라이언트 측 캐싱(브라우저, 프록시 서버, 네트워크 캐싱 시스템)과 내부 캐싱을 선택적으로 비활성화할 수 있습니다. [!DNL Platform Server] 캐시.

`cache= *`cacheControl`*`

`cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_70ACECAEA02F400C83B598FA13F1D00B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 설정|해제|유효성 검사|업데이트</span> </p> </td> 
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

하나만 `*`cacheControl`*` 값을 지정하면 클라이언트와 서버 캐시에 모두 적용됩니다.

다음 `validate` 키워드를 사용하면 캐시 항목이 자동으로 만료될 때까지 기다리지 않고 이미지 파일이 변경된 후에 캐시 항목을 업데이트할 수 있습니다. 클라이언트 캐싱은 이 명령의 영향을 받지 않습니다.

다음 `update` 키워드를 사용하여 서버측 캐시 항목을 강제로 업데이트할 수 있습니다. 이 기능은 파일 이름이나 관련 글꼴 ID를 변경하지 않고 글꼴 파일을 수정하는 경우와 같이 캐시 유효성 검사 메커니즘에서 직접 추적되지 않는 리소스를 변경한 후에 유용합니다.

중첩 요청에 지정된 경우, `cache=on` 중첩 요청으로 생성된 이미지의 서버측 영구 캐싱을 활성화합니다. 동일한 매개 변수를 사용하여 동일한 중첩 요청이 반복적으로 호출되어야 하는 경우에만 중첩 요청에 대해 캐싱을 활성화하려면 주의해야 합니다.

## 속성 {#section-dfd0b2f92b3743fc8b9d2c35a786eb81}

요청 속성입니다. 현재 레이어 설정에 관계없이 적용됩니다. 요청이 회신 이미지를 반환하지 않을 때 무시됩니다. *`clientControl`*이미지 카탈로그에서 클라이언트측 캐싱이 비활성화될 경우 무시됩니다. `catalog::Expiration` 에는 음수 값이 있습니다.)

클라이언트 측 캐시 제어( `on` 및 `off` 의 정적 컨텐츠 요청에 만 사용할 수 있습니다. [!DNL /is/content/].

## 기본값 {#section-4124b2c836e2491489b9009a92fe4f22}

`cache=on,on` HTTP 요청의 경우 `cache=off` 중첩/포함된 요청에 대해 `cache=on` 정적 콘텐츠 요청.

## 참조 {#section-7c2ac171fa0e4aa4a2e9955fd2d2013e}

[카탈로그::만료](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
