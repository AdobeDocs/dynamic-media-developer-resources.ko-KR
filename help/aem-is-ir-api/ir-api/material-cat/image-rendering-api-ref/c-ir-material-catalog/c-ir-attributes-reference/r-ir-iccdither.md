---
title: IccDither
description: 색상 변환 디더링. icc=로 명시적으로 선택하지 않은 경우 색상 변환의 가시 범위 품질을 개선하는 데 디더링을 사용할지 여부를 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bb1bec31-3f7c-48c8-9456-6359b739a657
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 3%

---

# IccDither{#iccdither}

색상 변환 디더링. `icc=`을(를) 사용하여 명시적으로 선택하지 않은 경우 색상 변환의 가시 범위 품질을 개선하는 데 디더링을 사용할지 여부를 지정합니다.

## 속성 {#section-646fb48084734c66bf648360f3a5bfd1}

플래그. 디더링을 비활성화하려면 `0`(으)로 설정하고, 디더링을 활성화하려면 `1`(으)로 설정합니다.

## 기본값 {#section-c9066c361215404d847f4d2c8f1ea3a5}

정의되지 않았거나 비어 있는 경우 `default::IccDither`에서 상속됩니다.

## 참조 {#section-76a376a1bee74670867b4de81fea65aa}

[attribute::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127) , [icc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)
