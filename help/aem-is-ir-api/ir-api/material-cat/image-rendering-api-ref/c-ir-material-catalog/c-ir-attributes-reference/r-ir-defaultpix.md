---
description: 기본 렌더링 이미지 크기. 요청이 wid= 또는 hei=를 사용하여 명시적으로 보기 크기를 지정하지 않는 경우 서버는 응답 이미지를 이 너비와 높이보다 크지 않도록 제한합니다.
seo-description: 기본 렌더링 이미지 크기. 요청이 wid= 또는 hei=를 사용하여 명시적으로 보기 크기를 지정하지 않는 경우 서버는 응답 이미지를 이 너비와 높이보다 크지 않도록 제한합니다.
seo-title: DefaultPix
solution: Experience Manager
title: DefaultPix
topic: Scene7 Image Serving - Image Rendering API
uuid: 27574811-a920-4e54-8635-5a643b8655ef
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# DefaultPix{#defaultpix}

기본 렌더링 이미지 크기. 요청이 wid= 또는 hei=를 사용하여 명시적으로 보기 크기를 지정하지 않는 경우 서버는 응답 이미지를 이 너비와 높이보다 크지 않도록 제한합니다.

## 속성 {#section-9dc5474fc75842308796ab6440b29611}

0보다 큰 정수 2개를 쉼표로 구분하여 지정합니다. 너비 및 높이(픽셀 단위) 두 값 중 하나 또는 둘 다 0으로 설정하여 제한을 해제할 수 있습니다.

중첩/임베디드 요청에는 적용되지 않습니다.

## 기본값 {#section-1935781c561e4679aa87a5bcced8df90}

정의되지 않았거나 비어 있는 `default::DefaultPix` 경우 상속됩니다.

## 참조 {#section-d28f18d29ef14692b8706ca08e754f54}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [속성::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)
