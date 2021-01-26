---
description: 색상 변환 렌더링 의도. 렌더링 의도가 icc=로 지정되지 않은 경우 색상 변환에 대한 기본 렌더링 의도를 제공합니다.
seo-description: 색상 변환 렌더링 의도. 렌더링 의도가 icc=로 지정되지 않은 경우 색상 변환에 대한 기본 렌더링 의도를 제공합니다.
seo-title: IccRenderIntent
solution: Experience Manager
title: IccRenderIntent
topic: Dynamic Media Image Serving - Image Rendering API
uuid: a9648405-32c3-4762-bbb2-11e97d4f8374
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 3%

---


# IccRenderIntent{#iccrenderintent}

색상 변환 렌더링 의도. 렌더링 의도가 icc=로 지정되지 않은 경우 색상 변환에 대한 기본 렌더링 의도를 제공합니다.

## 속성 {#section-0a38c60e1525426185616c42824aee2c}

열거형. 가시 가능의 경우 0으로, 상대 색도계의 경우 1로, 채도의 경우 2로, 절대 색도계의 경우 3으로 설정합니다. 색상 프로파일에 정의된 기본 렌더링 의도를 사용하려면 비워 두거나 다른 값으로 설정합니다.

## 기본값 {#section-9301e3b7d0184ec5bf54a6eb73a6d3c1}

정의되지 않은 경우 `default::IccRenderIntent`에서 상속됩니다. 비어 있으면 &#39;상대 색도계&#39;가 적용됩니다.

## 참조 {#section-e77bcdfef6d2486ebd545631ccb40ebd}

[특성::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127) ,  [속성::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0),  [icc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)
