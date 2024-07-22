---
description: 기본 썸네일 크기입니다. 썸네일 요청(req=tmb)에 대한 DefaultPix 속성 대신 사용됩니다.
solution: Experience Manager
title: DefaultThumbPix
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c1413da0-a68d-4345-928f-b532991966a8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 2%

---

# DefaultThumbPix{#defaultthumbpix}

기본 썸네일 크기입니다. 썸네일 요청(req=tmb)에 대해 attribute::DefaultPix 대신 사용됩니다.

썸네일 요청(`req=tmb`)이 크기를 명시적으로 지정하지 않고 `wid=`, `hei=` 또는 `scl=`을(를) 사용하여 보기 크기를 명시적으로 지정하지 않는 경우 서버에서 응답 이미지가 이 너비 및 높이보다 크지 않도록 제한합니다.

## 속성 {#section-650d9b1194fb4c47a03c6809e6b4af0e}

2개의 정수(0 이상)를 쉼표로 구분합니다. 폭 및 높이(픽셀 단위). 두 값 중 하나 또는 모두를 0으로 설정하여 구속을 해제할 수 있습니다.

중첩/포함된 요청에는 적용되지 않습니다.

## 기본값 {#section-2c4a4f14540449638822913513170ff1}

정의되지 않았거나 비어 있는 경우 `default::DefaultThumbPix`에서 상속됩니다.

## 참조 {#section-4ad00963ffa049fcb17ad63e6bbe7ac4}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [특성::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
