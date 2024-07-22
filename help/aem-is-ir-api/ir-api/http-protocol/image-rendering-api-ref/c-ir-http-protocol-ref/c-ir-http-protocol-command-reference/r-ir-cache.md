---
title: 캐시
description: 캐시 제어. 클라이언트측 캐싱(브라우저, 프록시 서버, 네트워크 캐싱 시스템)과 내부 [!DNL Platform Server] 캐시의 캐싱을 선택적으로 비활성화할 수 있습니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4745197a-9f2d-4e33-8c0e-0067fbd65254
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 1%

---

# 캐시 {#cache}

캐시 제어. 클라이언트 측 캐싱(브라우저, 프록시 서버, 네트워크 캐싱 시스템)과 내부 [!DNL Platform Server] 캐시의 캐싱을 선택적으로 비활성화할 수 있습니다.

`cache= *`cacheControl`*`

`cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_CBB5DFBD48B444A4AA806B11299BC43E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cacheControl</span> </p> </td> 
  <td class="stentry"> <p>날짜 | 끔 | 유효성 검사 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> clientControl </span> </p> </td> 
  <td class="stentry"> <p>날짜 | 끔 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> serverControl </span> </p></td> 
  <td class="stentry"> <p>날짜 | 끔 </p></td> 
 </tr> 
</table>

하나의 *`cacheControl`* 값만 지정된 경우 클라이언트 및 서버 캐시 모두에 적용됩니다.

&#39; `validate`&#39; 키워드를 사용하면 캐시 항목이 자동으로 만료될 때까지 기다릴 필요 없이 텍스처 또는 비네팅 파일이 변경된 후 서버 캐시 항목을 업데이트할 수 있습니다. 클라이언트 캐싱은 이 명령의 영향을 받지 않습니다.

중첩 요청에 지정된 경우 `cache=on`은(는) 중첩 요청으로 생성된 이미지의 영구적인 서버측 캐싱을 사용합니다. 동일한 중첩된 요청이 동일한 매개 변수를 사용하여 반복적으로 호출되는 경우에만 중첩된 요청에 대한 캐싱을 활성화해야 합니다.

## 속성 {#section-0dcbd62e1122400e8c347f408f2d937e}

요청의 어느 위치에서나 발생할 수 있습니다. 요청이 응답 이미지를 반환하지 않는 경우 무시됩니다. 재질 카탈로그에서 클라이언트측 캐싱을 사용하지 않도록 설정하면 *`clientControl`* 속성이 무시됩니다(`attribute::Expiration`에 음수 값이 있는 경우). 서버 캐싱을 사용하지 않도록 설정한 경우(`PlatformServer::cache.enable`) 속성 *`serverControl`*&#x200B;이(가) 무시됩니다.

## 기본값 {#section-9034a1f4d7984c8f8dce3fc1e1803723}

HTTP 요청의 경우 `cache=on,on`, 중첩/포함된 요청의 경우 `cache=off`.

## 참조 {#section-2f5853751dab49579e97418fa766bdf9}

[카탈로그::만료](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
