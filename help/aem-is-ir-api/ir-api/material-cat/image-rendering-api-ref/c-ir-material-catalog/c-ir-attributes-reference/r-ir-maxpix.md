---
title: MaxPix
description: 회신 이미지 크기 제한. 클라이언트에 반환될 수 있는 최대 회신 이미지 폭과 높이입니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48239519-7935-45e4-ae36-5e687a356cc1
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---

# MaxPix{#maxpix}

회신 이미지 크기 제한. 클라이언트에 반환될 수 있는 최대 회신 이미지 폭과 높이입니다.

폭과/또는 높이가 보다 큰 응답 이미지가 요청에 의해 반환되면 서버에서 오류를 반환합니다 `attribute::MaxSize`.

## 속성 {#section-390c1066b7a748aca3c0b45ad8bdcfb1}

0보다 큰 두 정수(쉼표로 구분) 너비와 높이(픽셀 단위)입니다. 제한 없이 회신 이미지 크기를 허용하기 위해 0,000으로 설정할 수도 있습니다.

## 기본값 {#section-45b38dc661854d11b97df5709f4f3434}

정의되지 않았거나 비어 있는 경우 기본값::MaxPix에서 상속됩니다.

## 참조 {#section-09cddedde91f43b1ac5828f7e3327c6a}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
