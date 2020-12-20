---
description: 이미지 높이를 회신합니다. 이미지의 종횡비를 유지하면서 응답 이미지의 높이가 지정된 값보다 크지 않도록 렌더링된 이미지의 비율을 지정합니다.
seo-description: 이미지 높이를 회신합니다. 이미지의 종횡비를 유지하면서 응답 이미지의 높이가 지정된 값보다 크지 않도록 렌더링된 이미지의 비율을 지정합니다.
seo-title: hei
solution: Experience Manager
title: hei
topic: Scene7 Image Serving - Image Rendering API
uuid: 616d3306-ccbd-4400-8a94-1ff6f47b802e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 2%

---


# hei{#hei}

이미지 높이를 회신합니다. 이미지의 종횡비를 유지하면서 응답 이미지의 높이가 지정된 값보다 크지 않도록 렌더링된 이미지의 비율을 지정합니다.

`hei= *`val`*`

<table id="simpletable_C3A31CA539DC4D9F8BE50290D1AFA5CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>이미지 높이를 픽셀 단위(0보다 큰 정수)로 회신합니다. </p></td> 
 </tr> 
</table>

`wid=` 및 `hei=`이 모두 지정되어 있고 너비/높이가 이미지의 종횡비와 다른 경우 이미지가 채워지지 않습니다.

`wid=` 서버 `hei=` 에서 반환되는 이미지의 크기를 정의하려면 함께 작업합니다. `scl=`이 URL에서 `wid=` 또는 `hei=` 뒤에 오는 경우 이러한 명령을 취소하고 `scl=`은 서버에서 반환되는 이미지의 크기를 정의합니다.

그러나 URL에서 `scl=` 뒤에 `wid=` 또는 `hei=`이 오는 경우 `scl=` 및 `wid=`/ `hei=`는 서버에서 반환되는 이미지의 크기를 정의합니다.

>[!NOTE]
>
>계산된 이미지 또는 기본 답글 이미지 크기가 `attribute::MaxPix`보다 크면 오류가 반환됩니다.

## 속성 {#section-6cbc6acd37c847beab84c896ac25280c}

요청 내 어느 곳에서든 발생할 수 있습니다. `wid=`, `hei=` 또는 `scl=`로 이미지 크기를 조정해도 응답 이미지에 포함된 인쇄 해상도 값이 변경되지 않습니다. 명령 시퀀스에서 `wid=` 및/또는 `hei=` 이후에 `scl=`이(가) 발생하는 경우 무시됩니다.

## 기본값 {#section-61043f6c1f5d450883ff9e5eafd95955}

`wid=`, `hei=` 또는 `scl=`가 지정되지 않은 경우 응답 이미지는 `attribute::DefaultPix`에 의해 정의된 크기 내에 맞게 크기가 조절됩니다. `attribute::DefaultPix`이(가) 비어 있으면 응답 이미지의 크기가 비네팅의 보기 이미지와 같습니다.

## 참조 {#section-7ba51379f1e2421c92d3592d20a37734}

[속성::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) ,  [속성::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657),  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)  [,resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
