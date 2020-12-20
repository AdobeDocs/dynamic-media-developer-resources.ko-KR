---
description: 비율 보기. 전체 해상도 비네팅을 기준으로 렌더링된 이미지의 크기를 지정된 비율 인수별로 조정합니다.
seo-description: 비율 보기. 전체 해상도 비네팅을 기준으로 렌더링된 이미지의 크기를 지정된 비율 인수별로 조정합니다.
seo-title: scl
solution: Experience Manager
title: scl
topic: Scene7 Image Serving - Image Rendering API
uuid: 04839c44-01b6-4fa2-9eda-bbb0f2822db4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 3%

---


# scl{#scl}

비율 보기. 전체 해상도 비네팅을 기준으로 렌더링된 이미지의 크기를 지정된 비율 인수별로 조정합니다.

`scl= *`invFactor`*`

<table id="simpletable_EFE352FA8EF14197B6934783A2883451"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> invFactor</span> </span> </p></td> 
  <td class="stentry"> <p>역배율 계수(실제, 1.0 이상). </p></td> 
 </tr> 
</table>

`scl=`이 URL에서 `wid=` 또는 `hei=` 뒤에 오는 경우 이러한 명령을 취소하고 `scl=`은 서버에서 반환되는 이미지의 크기를 정의합니다.

그러나 URL에서 `scl=` 뒤에 `wid=` 또는 `hei=`이 오는 경우 `scl=` 및 `wid=`/ `hei=`는 서버에서 반환되는 이미지의 크기를 정의합니다.

>[!NOTE]
>
>계산된 이미지 또는 기본 답글 이미지 크기가 `attribute::MaxPix`보다 크면 오류가 반환됩니다.

## 속성 {#section-170458cbd6984bd59a3434431258b20f}

요청 내 어느 곳에서든 발생할 수 있습니다. 명령 시퀀스에서 `scl=` 뒤에 `wid=` 또는 `hei=`이(가) 발생하는 경우 무시됩니다.

`scl=`으로 이미지 크기를 조정해도 응답 이미지에 포함된 인쇄 해상도 값은 변경되지 않습니다.

## 기본값 {#section-d47ab3fb5a7d486a9fc207904b3e70dd}

`wid=`, `hei=` 또는 `scl=`가 지정되지 않은 경우 응답 이미지는 `attribute::DefaultPix`에서 정의한 크기에 맞게 크기가 조절됩니다. `attribute::DefaultPix`이(가) 비어 있으면 응답 이미지의 크기가 비네팅의 보기 이미지와 같습니다.

## 참조 {#section-cc5002a1d49340bbb5c7a5864c297621}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) ,  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3),  [속성::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)  [, 속성::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)
