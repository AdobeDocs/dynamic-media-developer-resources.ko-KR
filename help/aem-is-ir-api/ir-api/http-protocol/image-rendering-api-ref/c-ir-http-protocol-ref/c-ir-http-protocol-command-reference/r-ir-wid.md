---
title: wid
description: 응답 이미지 너비. 이미지의 종횡비를 유지하면서 응답 이미지가 지정된 값보다 크지 않도록 렌더링된 이미지의 비율을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a77b71c3-8600-4d7a-ba52-e158cf9668eb
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 2%

---

# wid{#wid}

응답 이미지 너비. 이미지의 종횡비를 유지하면서 응답 이미지가 지정된 값보다 크지 않도록 렌더링된 이미지의 비율을 지정합니다.

`wid= *`val`*`

<table id="simpletable_1C898A7B99114BE986EC5553F6A31E82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>이미지 너비, 픽셀 단위(int가 0보다 큼). </p></td> 
 </tr> 
</table>

두 경우 모두 이미지에 패딩되지 않음 `wid=` 및 `hei=` 이(가) 지정되고 `wid`/ `hei` 는 이미지의 종횡비와 다릅니다.

`wid=` 및 `hei=` 함께 작업하여 서버에서 반환되는 이미지의 크기를 정의합니다. If `scl=` 다음 이후 `wid=` 또는 `hei=` url에서 해당 명령을 취소하고 `scl=` 서버에서 반환되는 이미지의 크기를 정의합니다.

그러나 다음과 같은 경우에는 `wid=` 또는 `hei=` 다음 이후 `scl=` url에서 취소됩니다. `scl=` 및 `wid=`/ `hei=` 서버에서 반환되는 이미지의 크기를 정의합니다.

>[!NOTE]
>
>계산 또는 기본 응답 이미지 크기가 보다 큰 경우 오류가 반환됩니다 `attribute::MaxPix`.

## 속성 {#section-2d067c6d371748e19cb157684700a49d}

요청 내의 어느 곳에서든 발생할 수 있습니다. 이미지 크기 조정 `wid=`, `hei=`, 또는 `scl=` 응답 이미지에 포함된 인쇄 해상도 값은 변경하지 않습니다. 다음과 같은 경우 무시됨 `scl=` 다음 이후 발생 `wid=` 또는 `hei=` 를 입력합니다.

## 기본값 {#section-c7c6efa03d864592a3398b6f1de5a0b0}

If `wid=`, `hei=`, 또는 `scl=` 을 지정하지 않으면 응답 이미지가 정의된 크기에 맞게 조정됩니다. `attribute::DefaultPix`. If `attribute::DefaultPix` 이(가) 비어 있으면 응답 이미지의 크기가 비네팅 보기 이미지와 같습니다.

## 참조 {#section-450dfc12b1d440e2a3172a69d91db51f}

[attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) , [속성::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
