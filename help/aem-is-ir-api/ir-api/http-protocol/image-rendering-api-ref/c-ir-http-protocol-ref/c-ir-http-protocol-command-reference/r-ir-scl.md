---
title: scl
description: 뷰 크기 조정. 전체 해상도 비네팅을 기준으로 지정된 배율 계수로 렌더링된 이미지의 비율을 조정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e36db25c-af45-4256-b982-b7b06b87f5f9
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '174'
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

If `scl=` 다음 시기 이후에 `wid=` 또는 `hei=` url에서 이 명령을 취소하고 `scl=` 서버가 반환한 이미지의 크기를 정의합니다.

그러나, `wid=` 또는 `hei=` 다음 시기 이후에 `scl=` URL에서 취소됩니다 `scl=` 및 `wid=`/ `hei=` 서버에서 반환한 이미지의 크기를 정의합니다.

>[!NOTE]
>
>계산된 이미지 또는 기본 회신 이미지 크기가 `attribute::MaxPix`.

## 속성 {#section-170458cbd6984bd59a3434431258b20f}

요청 내 어디에서나 발생할 수 있습니다. 다음 경우 무시됨 `wid=` 또는 `hei=` 다음 시기 이후에 `scl=` 명령 시퀀스에 있어야 합니다.

이미지 크기 조정 `scl=` 응답 이미지에 포함된 인쇄 해상도 값을 변경하지 않습니다.

## 기본값 {#section-d47ab3fb5a7d486a9fc207904b3e70dd}

If `wid=`, `hei=`, 또는 `scl=` 을 지정하지 않으면 회신 이미지가 정의된 크기에 맞게 조정됩니다. `attribute::DefaultPix`. If `attribute::DefaultPix` 가 비어 있으면, 응답 이미지의 크기가 비네트의 보기 이미지와 같습니다.

## 참조 {#section-cc5002a1d49340bbb5c7a5864c297621}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3), [속성::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)
