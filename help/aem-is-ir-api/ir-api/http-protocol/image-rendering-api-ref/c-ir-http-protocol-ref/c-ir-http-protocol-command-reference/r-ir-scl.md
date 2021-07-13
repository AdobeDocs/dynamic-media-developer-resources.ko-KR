---
description: 뷰 크기 조정. 전체 해상도 비네팅을 기준으로 지정된 배율 계수로 렌더링된 이미지의 비율을 조정합니다.
solution: Experience Manager
title: scl
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e36db25c-af45-4256-b982-b7b06b87f5f9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 3%

---

# scl{#scl}

뷰 크기 조정. 전체 해상도 비네팅을 기준으로 지정된 배율 계수로 렌더링된 이미지의 비율을 조정합니다.

`scl= *`invFactor`*`

<table id="simpletable_EFE352FA8EF14197B6934783A2883451"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> invFactor</span> </span> </p></td> 
  <td class="stentry"> <p>역배율 계수(실제, 1.0 이상) </p></td> 
 </tr> 
</table>

`scl=`이 URL에서 `wid=` 또는 `hei=` 다음에 오는 경우 해당 명령을 취소하고 `scl=`에서 서버에서 반환되는 이미지의 크기를 정의합니다.

그러나 `wid=` 또는 `hei=`이 URL에서 `scl=` 다음에 오는 경우 `scl=` 및 `wid=`/ `hei=`는 서버에서 반환되는 이미지의 크기를 정의합니다.

>[!NOTE]
>
>계산 또는 기본 회신 이미지 크기가 `attribute::MaxPix`보다 큰 경우 오류가 반환됩니다.

## 속성 {#section-170458cbd6984bd59a3434431258b20f}

요청 내 어디에서나 발생할 수 있습니다. 명령 시퀀스에서 `scl=` 다음에 `wid=` 또는 `hei=`이 발생하면 무시됩니다.

`scl=`으로 이미지 크기를 조정해도 응답 이미지에 포함된 인쇄 해상도 값이 변경되지 않습니다.

## 기본값 {#section-d47ab3fb5a7d486a9fc207904b3e70dd}

`wid=`, `hei=` 및 `scl=`를 지정하지 않은 경우 응답 이미지가 `attribute::DefaultPix`에 정의된 크기 내에 맞게 조정됩니다. `attribute::DefaultPix`이 비어 있으면 회신 이미지의 크기가 비네트의 보기 이미지와 같습니다.

## 참조 {#section-cc5002a1d49340bbb5c7a5864c297621}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) ,  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3),  [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657),  [attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)
