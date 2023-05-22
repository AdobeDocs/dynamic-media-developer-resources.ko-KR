---
title: DefaultPix
description: 기본 렌더링 이미지 크기입니다. 요청에서 wid= 또는 hei=를 사용하여 보기 크기를 명시적으로 지정하지 않을 경우 서버에서 응답 이미지가 이 너비 및 높이보다 크지 않도록 제한합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d60f2b8c-5213-42ad-8ec9-7e7797d74e09
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 2%

---

# DefaultPix{#defaultpix}

기본 렌더링 이미지 크기입니다. 요청에서 wid= 또는 hei=를 사용하여 보기 크기를 명시적으로 지정하지 않을 경우 서버에서 응답 이미지가 이 너비 및 높이보다 크지 않도록 제한합니다.

## 속성 {#section-9dc5474fc75842308796ab6440b29611}

2개의 정수(0 이상)를 쉼표로 구분합니다. 폭 및 높이(픽셀 단위). 두 값 중 하나 또는 모두를 0으로 설정하여 구속을 해제할 수 있습니다.

중첩/포함된 요청에는 적용할 수 없습니다.

## 기본값 {#section-1935781c561e4679aa87a5bcced8df90}

상속 위치 `default::DefaultPix` 정의되지 않은 경우 또는 비어 있는 경우.

## 참조 {#section-d28f18d29ef14692b8706ca08e754f54}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)
