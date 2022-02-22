---
title: pathEmbed
description: 경로 데이터를 포함합니다. 비네트에 포함된 Photoshop 경로를 응답 이미지에 포함할지 여부를 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 66cc57ef-964e-4062-bb66-efeda15be744
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---

# pathEmbed{#pathembed}

경로 데이터를 포함합니다. 비네트에 포함된 Photoshop 경로를 응답 이미지에 포함할지 여부를 지정합니다.

`pathEmbed=0|1`

## 속성 {#section-be50b6d1ebd14a9c93f80ac338b44bfc}

요청 속성입니다. 비네트에 경로 데이터가 포함되지 않은 경우 무시됩니다. 경로 데이터의 크기가 `wid=` 및/또는 `hei=` 필요한 경우

출력 이미지 형식이 경로 포함을 지원하지 않는 경우에는 무시됩니다. 의 설명을 참조하십시오. `fmt=` 경로 포함을 지원하는 출력 이미지 형식 목록입니다.

## 기본값 {#section-3be88ed9053b48919ff33af9418078cc}

`pathEmbed=0`를 사용하도록 선택할 수 있습니다.

## 참조 {#section-4e6151658c384b6f9d0446f55dde7b7f}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
