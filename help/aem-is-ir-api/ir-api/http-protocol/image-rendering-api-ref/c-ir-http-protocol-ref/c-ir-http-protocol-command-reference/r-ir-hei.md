---
description: 응답 이미지 높이입니다. 이미지의 종횡비를 유지하면서 응답 이미지의 높이가 지정된 값보다 크지 않도록 렌더링된 이미지의 비율을 지정합니다.
seo-description: 응답 이미지 높이입니다. 이미지의 종횡비를 유지하면서 응답 이미지의 높이가 지정된 값보다 크지 않도록 렌더링된 이미지의 비율을 지정합니다.
seo-title: hei
solution: Experience Manager
title: hei
topic: Scene7 Image Serving - Image Rendering API
uuid: 616d3306-ccbd-4400-8a94-1ff6f47b802e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# hei{#hei}

응답 이미지 높이입니다. 이미지의 종횡비를 유지하면서 응답 이미지의 높이가 지정된 값보다 크지 않도록 렌더링된 이미지의 비율을 지정합니다.

`hei= *`val`*`

<table id="simpletable_C3A31CA539DC4D9F8BE50290D1AFA5CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 값</span></span> </p></td> 
  <td class="stentry"> <p>이미지 높이(픽셀 단위: 0보다 큰 정수) </p></td> 
 </tr> 
</table>

둘 다 `wid=` `hei=` 지정하고 폭/높이가 이미지의 종횡비와 다를 경우 이미지가 채워지지 않습니다.

`wid=` 함께 `hei=` 작업하여 서버에서 반환되는 이미지의 크기를 정의합니다. URL 뒤에 `scl=` 오는 `wid=` 경우 해당 명령을 취소하고 서버에서 반환된 이미지의 크기를 `hei=` `scl=` 정의합니다.

그러나 URL 뒤에 `wid=` 또는 `hei=` 오는 `scl=` 경우 서버가 반환한 이미지의 크기를 취소하고 `scl=``wid=``hei=` 정의합니다.

>[!NOTE]
>
>계산된 이미지 또는 기본 회신 이미지 크기가 `attribute::MaxPix`다음보다 큰 경우 오류가 반환됩니다.

## 속성 {#section-6cbc6acd37c847beab84c896ac25280c}

요청 내 어느 곳에서나 발생할 수 있습니다. 응답 이미지에 임베드된 인쇄 해상도 값을 `wid=`사용하거나 `hei=`변경하지 `scl=` 않고 이미지 크기를 조정합니다. 명령 시퀀스의 이후 `scl=` 및/ `wid=` `hei=` 또는 후에 발생하는 경우 무시됩니다.

## 기본값 {#section-61043f6c1f5d450883ff9e5eafd95955}

둘 중 하나 `wid=`또는 둘 다 지정하지 않으면 응답 이미지의 크기가 `hei=``scl=` `attribute::DefaultPix`정의된 크기에 맞게 조절됩니다. 비어 `attribute::DefaultPix` 있으면 응답 이미지의 크기가 비네팅의 보기 이미지와 같습니다.

## 참조 {#section-7ba51379f1e2421c92d3592d20a37734}

[attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) , [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)[, resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
