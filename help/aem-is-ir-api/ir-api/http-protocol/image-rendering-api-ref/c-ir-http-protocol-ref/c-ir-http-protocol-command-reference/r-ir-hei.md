---
description: 이미지 높이를 회신합니다. 이미지의 종횡비를 유지하면서 응답 이미지의 높이가 지정된 값보다 크지 않도록 렌더링된 이미지의 비율을 지정합니다.
solution: Experience Manager
title: hei
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 8e93aa32-b38e-46e4-be52-abd81222cfc3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 2%

---

# 헤이{#hei}

이미지 높이를 회신합니다. 이미지의 종횡비를 유지하면서 응답 이미지의 높이가 지정된 값보다 크지 않도록 렌더링된 이미지의 비율을 지정합니다.

`hei= *`val`*`

<table id="simpletable_C3A31CA539DC4D9F8BE50290D1AFA5CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>이미지 높이(픽셀 단위)를 회신합니다(0보다 큰 정수). </p></td> 
 </tr> 
</table>

`wid=` 및 `hei=` 둘 다 지정되고 너비/높이가 이미지의 종횡비와 다른 경우 이미지가 채워지지 않습니다.

`wid=` 및  `hei=` 를 함께 사용하여 서버에서 반환되는 이미지의 크기를 정의합니다. `scl=`이 URL에서 `wid=` 또는 `hei=` 다음에 오는 경우 해당 명령을 취소하고 `scl=`에서 서버에서 반환되는 이미지의 크기를 정의합니다.

그러나 `wid=` 또는 `hei=`이 URL에서 `scl=` 다음에 오는 경우 `scl=` 및 `wid=`/ `hei=`는 서버에서 반환되는 이미지의 크기를 정의합니다.

>[!NOTE]
>
>계산 또는 기본 회신 이미지 크기가 `attribute::MaxPix`보다 큰 경우 오류가 반환됩니다.

## 속성 {#section-6cbc6acd37c847beab84c896ac25280c}

요청 내 어디에서나 발생할 수 있습니다. `wid=`, `hei=` 또는 `scl=`로 이미지 크기를 조정해도 응답 이미지에 포함된 인쇄 해상도 값이 변경되지 않습니다. 명령 시퀀스에서 `wid=` 및/또는 `hei=` 이후에 `scl=`이 발생하면 무시됩니다.

## 기본값 {#section-61043f6c1f5d450883ff9e5eafd95955}

`wid=`, `hei=` 및 `scl=`를 지정하지 않은 경우 응답 이미지가 `attribute::DefaultPix`에 정의된 크기 내에 맞게 조정됩니다. `attribute::DefaultPix`이 비어 있으면 회신 이미지의 크기가 비네트의 보기 이미지와 같습니다.

## 참조 {#section-7ba51379f1e2421c92d3592d20a37734}

[attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) ,  [속성::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657),  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29),  [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
