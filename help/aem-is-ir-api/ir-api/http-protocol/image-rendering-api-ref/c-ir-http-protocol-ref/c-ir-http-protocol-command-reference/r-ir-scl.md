---
title: scl
description: 크기 조절 보기. 전체 해상도 비네팅을 기준으로 지정된 배율 인자로 렌더링된 이미지의 배율을 조정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e36db25c-af45-4256-b982-b7b06b87f5f9
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 1%

---

# scl{#scl}

크기 조절 보기. 전체 해상도 비네팅을 기준으로 지정된 배율 인자로 렌더링된 이미지의 배율을 조정합니다.

`scl= *`invFactor`*`

<table id="simpletable_EFE352FA8EF14197B6934783A2883451"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> invFactor</span> </span> </p></td> 
  <td class="stentry"> <p>역배율 계수(실수, 1.0 이상). </p></td> 
 </tr> 
</table>

`scl=`이(가) URL에서 `wid=` 또는 `hei=` 다음에 오면 해당 명령이 취소되고 `scl=`은(는) 서버에서 반환되는 이미지의 크기를 정의합니다.

그러나 URL에서 `wid=` 또는 `hei=`이(가) `scl=` 뒤에 오면 `scl=`을(를) 취소하고 `wid=`/ `hei=`을(를) 통해 서버에서 반환되는 이미지 크기를 정의합니다.

>[!NOTE]
>
>계산 또는 기본 응답 이미지 크기가 `attribute::MaxPix`보다 큰 경우 오류가 반환됩니다.

## 속성 {#section-170458cbd6984bd59a3434431258b20f}

요청 내의 어느 곳에서든 발생할 수 있습니다. 명령 시퀀스에서 `scl=` 다음에 `wid=` 또는 `hei=`이(가) 발생하는 경우 무시됩니다.

`scl=`(으)로 이미지 크기를 조정해도 응답 이미지에 포함된 인쇄 해상도 값은 변경되지 않습니다.

## 기본값 {#section-d47ab3fb5a7d486a9fc207904b3e70dd}

`wid=`, `hei=` 또는 `scl=`을(를) 지정하지 않으면 응답 이미지가 `attribute::DefaultPix`에 정의된 크기에 맞게 조정됩니다. `attribute::DefaultPix`이(가) 비어 있으면 응답 이미지의 크기가 비네팅 보기 이미지와 같습니다.

## 참조 {#section-cc5002a1d49340bbb5c7a5864c297621}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3), [특성::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [특성::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)
