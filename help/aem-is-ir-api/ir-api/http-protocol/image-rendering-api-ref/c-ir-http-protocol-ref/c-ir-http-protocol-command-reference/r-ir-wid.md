---
description: 회신 이미지 너비. 이미지의 종횡비를 유지하면서 응답 이미지가 지정된 값보다 크지 않도록 렌더링된 이미지의 비율을 지정합니다.
solution: Experience Manager
title: wid
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a77b71c3-8600-4d7a-ba52-e158cf9668eb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 2%

---

# wid{#wid}

회신 이미지 너비. 이미지의 종횡비를 유지하면서 응답 이미지가 지정된 값보다 크지 않도록 렌더링된 이미지의 비율을 지정합니다.

`wid= *`val`*`

<table id="simpletable_1C898A7B99114BE986EC5553F6A31E82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>이미지 너비(픽셀 단위)가 0보다 큼. </p></td> 
 </tr> 
</table>

`wid=` 및 `hei=` 둘 다 지정되고 `wid`/ `hei`가 이미지의 종횡비와 다른 경우 이미지가 채워지지 않습니다.

`wid=` 및  `hei=` 를 함께 사용하여 서버에서 반환되는 이미지의 크기를 정의합니다. `scl=`이 URL에서 `wid=` 또는 `hei=` 다음에 오는 경우 해당 명령을 취소하고 `scl=`에서 서버에서 반환되는 이미지의 크기를 정의합니다.

그러나 `wid=` 또는 `hei=`이 URL에서 `scl=` 다음에 오는 경우 `scl=` 및 `wid=`/ `hei=`는 서버에서 반환되는 이미지의 크기를 정의합니다.

>[!NOTE]
>
>계산 또는 기본 회신 이미지 크기가 `attribute::MaxPix`보다 큰 경우 오류가 반환됩니다.

## 속성 {#section-2d067c6d371748e19cb157684700a49d}

요청 내 어디에서나 발생할 수 있습니다. `wid=`, `hei=` 또는 `scl=`로 이미지 크기를 조정해도 응답 이미지에 포함된 인쇄 해상도 값이 변경되지 않습니다. 명령 시퀀스에서 `wid=` 또는 `hei=` 다음에 `scl=`이 발생하면 무시됩니다.

## 기본값 {#section-c7c6efa03d864592a3398b6f1de5a0b0}

`wid=`, `hei=` 및 `scl=`를 지정하지 않은 경우 응답 이미지가 `attribute::DefaultPix`에 정의된 크기 내에 맞게 조정됩니다. `attribute::DefaultPix`이 비어 있으면 회신 이미지의 크기가 비네트의 보기 이미지와 같습니다.

## 참조 {#section-450dfc12b1d440e2a3172a69d91db51f}

[attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) ,  [속성::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29),  [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
