---
title: hei
description: 응답 이미지 높이입니다. 이미지의 종횡비를 유지하면서 응답 이미지의 높이가 지정된 값보다 크지 않도록 렌더링된 이미지의 비율을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8e93aa32-b38e-46e4-be52-abd81222cfc3
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 2%

---

# hei{#hei}

응답 이미지 높이입니다. 이미지의 종횡비를 유지하면서 응답 이미지의 높이가 지정된 값보다 크지 않도록 렌더링된 이미지의 비율을 지정합니다.

`hei= *`val`*`

<table id="simpletable_C3A31CA539DC4D9F8BE50290D1AFA5CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>응답 이미지 높이(픽셀 단위)입니다(0보다 큰 정수). </p></td> 
 </tr> 
</table>

두 경우 모두 이미지에 패딩되지 않음 `wid=` 및 `hei=` 가 지정되고 너비/높이가 이미지의 종횡비와 다릅니다.

`wid=` 및 `hei=` 함께 작업하여 서버에서 반환되는 이미지의 크기를 정의합니다. If `scl=` 다음 이후 `wid=` 또는 `hei=` url에서 해당 명령을 취소하고 `scl=` 서버에서 반환되는 이미지의 크기를 정의합니다.

그러나 다음과 같은 경우에는 `wid=` 또는 `hei=` 다음 이후 `scl=` url에서 취소됩니다. `scl=` 및 `wid=`/ `hei=` 서버에서 반환되는 이미지의 크기를 정의합니다.

>[!NOTE]
>
>계산 또는 기본 응답 이미지 크기가 보다 큰 경우 오류가 반환됩니다 `attribute::MaxPix`.

## 속성 {#section-6cbc6acd37c847beab84c896ac25280c}

요청 내의 어느 곳에서든 발생할 수 있습니다. 이미지 크기 조정 `wid=`, `hei=`, 또는 `scl=` 응답 이미지에 포함된 인쇄 해상도 값은 변경하지 않습니다. 다음과 같은 경우 무시됨 `scl=` 다음 이후 발생 `wid=` 및/또는 `hei=` 를 입력합니다.

## 기본값 {#section-61043f6c1f5d450883ff9e5eafd95955}

If `wid=`, `hei=`, 또는 `scl=` 을 지정하지 않으면 응답 이미지가 정의된 크기에 맞게 조정됩니다. `attribute::DefaultPix`. If `attribute::DefaultPix` 이(가) 비어 있으면 응답 이미지의 크기가 비네팅 보기 이미지와 같습니다.

## 참조 {#section-7ba51379f1e2421c92d3592d20a37734}

[attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) , [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
