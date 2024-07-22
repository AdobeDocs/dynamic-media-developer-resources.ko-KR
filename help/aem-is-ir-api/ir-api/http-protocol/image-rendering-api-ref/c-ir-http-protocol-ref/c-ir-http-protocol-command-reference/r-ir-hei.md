---
title: hei
description: 응답 이미지 높이입니다. 이미지의 종횡비를 유지하면서 응답 이미지의 높이가 지정된 값보다 크지 않도록 렌더링된 이미지의 비율을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8e93aa32-b38e-46e4-be52-abd81222cfc3
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 1%

---

# hei{#hei}

응답 이미지 높이입니다. 이미지의 종횡비를 유지하면서 응답 이미지의 높이가 지정된 값보다 크지 않도록 렌더링된 이미지의 비율을 지정합니다.

`hei= *`val`*`

<table id="simpletable_C3A31CA539DC4D9F8BE50290D1AFA5CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 값</span> </span> </p></td> 
  <td class="stentry"> <p>응답 이미지 높이(픽셀 단위)입니다(0보다 큰 정수). </p></td> 
 </tr> 
</table>

`wid=`과(와) `hei=`이(가) 모두 지정되어 있고 너비/높이가 이미지의 종횡비와 다른 경우 이미지가 패딩되지 않습니다.

`wid=`과(와) `hei=`이(가) 함께 작동하여 서버에서 반환되는 이미지의 크기를 정의합니다. `scl=`이(가) URL에서 `wid=` 또는 `hei=` 다음에 오면 해당 명령이 취소되고 `scl=`은(는) 서버에서 반환되는 이미지의 크기를 정의합니다.

그러나 URL에서 `wid=` 또는 `hei=`이(가) `scl=` 뒤에 오면 `scl=`을(를) 취소하고 `wid=`/ `hei=`을(를) 통해 서버에서 반환되는 이미지 크기를 정의합니다.

>[!NOTE]
>
>계산 또는 기본 응답 이미지 크기가 `attribute::MaxPix`보다 큰 경우 오류가 반환됩니다.

## 속성 {#section-6cbc6acd37c847beab84c896ac25280c}

요청 내의 어느 곳에서든 발생할 수 있습니다. `wid=`, `hei=` 또는 `scl=`(으)로 이미지 크기를 조정해도 응답 이미지에 포함된 인쇄 해상도 값은 변경되지 않습니다. 명령 시퀀스에서 `wid=` 및/또는 `hei=` 이후에 `scl=`이(가) 발생하는 경우 무시됩니다.

## 기본값 {#section-61043f6c1f5d450883ff9e5eafd95955}

`wid=`, `hei=` 또는 `scl=`을(를) 지정하지 않으면 응답 이미지가 `attribute::DefaultPix`에 정의된 크기에 맞게 조정됩니다. `attribute::DefaultPix`이(가) 비어 있으면 응답 이미지의 크기가 비네팅 보기 이미지와 같습니다.

## 참조 {#section-7ba51379f1e2421c92d3592d20a37734}

[특성::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) , [특성::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
