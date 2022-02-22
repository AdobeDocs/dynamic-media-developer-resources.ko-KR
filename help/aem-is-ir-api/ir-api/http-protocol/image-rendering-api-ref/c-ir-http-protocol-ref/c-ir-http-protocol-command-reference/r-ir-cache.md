---
title: 캐시
description: 캐시 제어. 내부 Platform Server 캐시에서 클라이언트 측 캐싱(브라우저, 프록시 서버, 네트워크 캐싱 시스템)과 캐싱을 선택적으로 비활성화할 수 있습니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4745197a-9f2d-4e33-8c0e-0067fbd65254
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 1%

---

# 캐시 {#cache}

캐시 제어. 내부 Platform Server 캐시에서 클라이언트 측 캐싱(브라우저, 프록시 서버, 네트워크 캐싱 시스템) 및 캐싱을 선택적으로 비활성화할 수 있습니다.

`cache= *`cacheControl`*`

`cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_CBB5DFBD48B444A4AA806B11299BC43E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cacheControl</span> </p> </td> 
  <td class="stentry"> <p>on | 해제 | 유효성 검사 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> clientControl </span> </p> </td> 
  <td class="stentry"> <p>on | 해제 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> serverControl </span> </p></td> 
  <td class="stentry"> <p>on | 해제 </p></td> 
 </tr> 
</table>

하나만 *`cacheControl`* 값을 지정하면 클라이언트와 서버 캐시에 모두 적용됩니다.

&#39; `validate`&#39; 키워드를 사용하면 캐시 항목이 자동으로 만료될 때까지 기다리지 않고 텍스쳐 또는 비네팅 파일이 변경된 후에 서버 캐시 항목을 업데이트할 수 있습니다. 클라이언트 캐싱은 이 명령의 영향을 받지 않습니다.

중첩 요청에 지정된 경우, `cache=on` 중첩 요청으로 생성된 이미지의 서버측 영구 캐싱을 활성화합니다. 동일한 매개 변수를 사용하여 동일한 중첩 요청이 반복적으로 호출되는 경우에만 중첩 요청에 대해 캐싱을 활성화하도록 하십시오.

## 속성 {#section-0dcbd62e1122400e8c347f408f2d937e}

은 요청의 모든 위치에서 발생할 수 있습니다. 요청이 회신 이미지를 반환하지 않을 때 무시됩니다. 속성 *`clientControl`* 재료 카탈로그에 의해 클라이언트측 캐싱이 비활성화되면 무시됩니다(인 경우 `attribute::Expiration` 에는 음수 값이 있습니다.) 속성 *`serverControl`* 서버 캐싱이 비활성화된 경우 무시됩니다( `PlatformServer::cache.enable`).

## 기본값 {#section-9034a1f4d7984c8f8dce3fc1e1803723}

`cache=on,on` HTTP 요청의 경우 `cache=off` 중첩된/포함된 요청에 대해 사용됩니다.

## 참조 {#section-2f5853751dab49579e97418fa766bdf9}

[카탈로그::만료](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
