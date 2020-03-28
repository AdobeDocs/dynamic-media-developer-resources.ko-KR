---
description: 기본 축소판 크기 축소판 요청에 대해 DefaultPix 속성 대신 사용됩니다(req=tmb).
seo-description: 기본 축소판 크기 축소판 요청에 대해 DefaultPix 속성 대신 사용됩니다(req=tmb).
seo-title: DefaultThumbPix
solution: Experience Manager
title: DefaultThumbPix
topic: Scene7 Image Serving - Image Rendering API
uuid: 7b310aab-6d38-45f3-a3e7-b074a8e7a795
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# DefaultThumbPix{#defaultthumbpix}

기본 축소판 크기 축소판 요청에 대해 attribute::DefaultPix 대신 사용됩니다(req=tmb).

축소판 요청( `req=tmb`)이 보기 크기를 명시적으로 지정하지 않은 경우 서버는 응답 이미지를 이 폭 및 높이보다 크지 않도록 제한합니다. 단, `wid=``hei=`또는 `scl=`을 사용하여 명시적으로 보기 크기를 지정하지 않습니다.

## 속성 {#section-650d9b1194fb4c47a03c6809e6b4af0e}

0보다 큰 정수 2개를 쉼표로 구분하여 지정합니다. 너비 및 높이(픽셀 단위) 두 값 중 하나 또는 둘 다 0으로 설정하여 제한을 해제할 수 있습니다.

중첩/임베디드 요청에는 적용되지 않습니다.

## 기본값 {#section-2c4a4f14540449638822913513170ff1}

정의되지 않았거나 비어 있는 `default::DefaultThumbPix` 경우 상속됩니다.

## 참조 {#section-4ad00963ffa049fcb17ad63e6bbe7ac4}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [속성::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
