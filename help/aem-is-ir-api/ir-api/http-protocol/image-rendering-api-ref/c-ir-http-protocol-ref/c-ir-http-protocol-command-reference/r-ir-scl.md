---
description: 확대 보기. 전체 해상도 비네팅을 기준으로 지정된 비율 인수를 기준으로 렌더링된 이미지의 크기를 조정합니다.
seo-description: 확대 보기. 전체 해상도 비네팅을 기준으로 지정된 비율 인수를 기준으로 렌더링된 이미지의 크기를 조정합니다.
seo-title: scl
solution: Experience Manager
title: scl
topic: Scene7 Image Serving - Image Rendering API
uuid: 04839c44-01b6-4fa2-9eda-bbb0f2822db4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# scl{#scl}

확대 보기. 전체 해상도 비네팅을 기준으로 지정된 비율 인수를 기준으로 렌더링된 이미지의 크기를 조정합니다.

`scl= *`invFactor`*`

<table id="simpletable_EFE352FA8EF14197B6934783A2883451"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> invFactor</span></span> </p></td> 
  <td class="stentry"> <p>역배율 인수(실제, 1.0 이상). </p></td> 
 </tr> 
</table>

URL 뒤에 `scl=` 오는 `wid=` 경우 해당 명령을 취소하고 서버에서 반환된 이미지의 크기를 `hei=` `scl=` 정의합니다.

그러나 URL 뒤에 `wid=` 또는 `hei=` 오는 `scl=` 경우 서버가 반환한 이미지의 크기를 취소하고 `scl=``wid=``hei=` 정의합니다.

>[!NOTE]
>
>계산된 이미지 또는 기본 회신 이미지 크기가 `attribute::MaxPix`다음보다 큰 경우 오류가 반환됩니다.

## 속성 {#section-170458cbd6984bd59a3434431258b20f}

요청 내 어느 곳에서나 발생할 수 있습니다. 명령 시퀀스의 뒤에 `wid=` 발생하거나 `hei=` 발생한 경우 `scl=` 무시됩니다.

이미지 크기를 조정해도 응답 이미지에 임베드된 인쇄 해상도 값이 변경되지 `scl=` 않습니다.

## 기본값 {#section-d47ab3fb5a7d486a9fc207904b3e70dd}

둘 다 `wid=`지정되지 `hei=` 않거나 `scl=` `attribute::DefaultPix`지정하지 않으면 응답 이미지가 정의된 크기 내에 맞게 조정됩니다. 비어 `attribute::DefaultPix` 있으면 응답 이미지의 크기가 비네팅의 보기 이미지와 같습니다.

## 참조 {#section-cc5002a1d49340bbb5c7a5864c297621}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3), [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)[, attribute::Default Pix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)
