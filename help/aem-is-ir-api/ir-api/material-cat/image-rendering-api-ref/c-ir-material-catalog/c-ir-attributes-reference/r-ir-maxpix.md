---
title: MaxPix
description: 응답 이미지 크기 제한. 클라이언트로 반환할 수 있는 응답 이미지의 최대 너비 및 높이입니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48239519-7935-45e4-ae36-5e687a356cc1
TQID: 'https://experienceleague.adobe.com/pgrg9BCY7fJXGsoABNjMOwIhRxYzrmQpsDSyGd6GSCc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 103
ht-degree: 2%

---

# MaxPix{#maxpix}

응답 이미지 크기 제한. 클라이언트로 반환할 수 있는 응답 이미지의 최대 너비 및 높이입니다.

요청으로 인해 너비 및/또는 높이가 `attribute::MaxSize`보다 큰 응답 이미지가 발생하는 경우 서버에서 오류를 반환합니다.

## 속성 {#section-390c1066b7a748aca3c0b45ad8bdcfb1}

0보다 큰 두 개의 정수를 쉼표로 구분합니다. 폭 및 높이(픽셀 단위). 응답 이미지 크기를 제한 없이 허용하려면 0,0으로 설정할 수도 있습니다.

## 기본값 {#section-45b38dc661854d11b97df5709f4f3434}

정의되지 않았거나 비어 있는 경우 기본값::MaxPix에서 상속됩니다.

## 참조 {#section-09cddedde91f43b1ac5828f7e3327c6a}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)

