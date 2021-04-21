---
description: 이미지 크기 제한에 회신합니다. 클라이언트에 반환될 수 있는 최대 응답 이미지 폭과 높이입니다.
solution: Experience Manager
title: MaxPix
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---


# MaxPix{#maxpix}

이미지 크기 제한에 회신합니다. 클라이언트에 반환될 수 있는 최대 응답 이미지 폭과 높이입니다.

요청 시 너비 및/또는 높이가 `attribute::MaxSize`보다 큰 응답 이미지가 표시되는 경우 서버가 오류를 반환합니다.

## 속성 {#section-390c1066b7a748aca3c0b45ad8bdcfb1}

0보다 큰 정수 2개를 쉼표로 구분하여 입력합니다. 폭과 높이(픽셀 단위) 회신 이미지 크기를 제한 없이 허용하려면 0으로 설정할 수도 있습니다.

## 기본값 {#section-45b38dc661854d11b97df5709f4f3434}

기본값이 정의되지 않았거나 비어 있는 경우::MaxPix에서 상속됩니다.

## 참조 {#section-09cddedde91f43b1ac5828f7e3327c6a}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) ,  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
