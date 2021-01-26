---
description: 캐시 제어. 선택적으로 클라이언트측 캐싱(브라우저, 프록시 서버, 네트워크 캐싱 시스템)을 비활성화하고 내부 플랫폼 서버 캐시에서 캐싱을 수행할 수 있습니다.
seo-description: 캐시 제어. 선택적으로 클라이언트측 캐싱(브라우저, 프록시 서버, 네트워크 캐싱 시스템)을 비활성화하고 내부 플랫폼 서버 캐시에서 캐싱을 수행할 수 있습니다.
seo-title: 캐시
solution: Experience Manager
title: 캐시
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 8af89b67-39d5-43e5-a58d-2cd509a1e373
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 1%

---


# 캐시{#cache}

캐시 제어. 선택적으로 클라이언트측 캐싱(브라우저, 프록시 서버, 네트워크 캐싱 시스템)을 비활성화하고 내부 플랫폼 서버 캐시에서 캐싱을 수행할 수 있습니다.

`cache= *`cacheControl`*`

`cache= *``*, *`clientControlserverControl`*`

<table id="simpletable_CBB5DFBD48B444A4AA806B11299BC43E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cacheControl</span> </p> </td> 
  <td class="stentry"> <p>on | 해제 | 유효성 검사 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> clientControl  </span> </p> </td> 
  <td class="stentry"> <p>on | 해제 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> serverControl  </span> </p></td> 
  <td class="stentry"> <p>on | 해제 </p></td> 
 </tr> 
</table>

*`cacheControl`* 값을 하나만 지정하면 클라이언트와 서버 캐시 모두에 적용됩니다.

&#39; `validate`&#39; 키워드를 사용하면 캐시 항목이 자동으로 만료될 때까지 기다릴 필요 없이 텍스처 또는 비네팅 파일이 변경된 후 서버 캐시 항목을 업데이트할 수 있습니다. 클라이언트 캐싱은 이 명령의 영향을 받지 않습니다.

중첩 요청에 지정된 경우, `cache=on`은 중첩된 요청에 의해 생성된 이미지의 서버측 지속적인 캐싱을 활성화합니다. 동일한 매개 변수를 사용하여 동일한 중첩 요청을 반복적으로 호출해야 하는 경우에만 중첩된 요청에 대해 캐싱을 활성화하는 것이 좋습니다.

## 속성 {#section-0dcbd62e1122400e8c347f408f2d937e}

요청에서 어느 곳에서나 발생할 수 있습니다. 요청이 응답 이미지를 반환하지 않을 때 무시됩니다. *`clientControl`* 은 재질 카탈로그에서 클라이언트측 캐싱을 비활성화하면 무시됩니다(음수 값이  `attribute::Expiration` 있는 경우). *`serverControl`* 서버 캐싱이 비활성화된 경우() 가  `PlatformServer::cache.enable`무시됩니다.

## 기본값 {#section-9034a1f4d7984c8f8dce3fc1e1803723}

`cache=on,on` HTTP 요청에 대해 중첩/ `cache=off` 포함된 요청에 대해 설명합니다.

## 참조 {#section-2f5853751dab49579e97418fa766bdf9}

[카탈로그::만료](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
