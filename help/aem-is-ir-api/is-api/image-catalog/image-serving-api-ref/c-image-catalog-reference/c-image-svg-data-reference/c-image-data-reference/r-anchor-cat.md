---
description: 이미지 앵커. 이 이미지가 템플릿 또는 합성 이미지에서 레이어로 사용될 경우 원점을 나타냅니다.
seo-description: 이미지 앵커. 이 이미지가 템플릿 또는 합성 이미지에서 레이어로 사용될 경우 원점을 나타냅니다.
seo-title: 앵커
solution: Experience Manager
title: 앵커
topic: Scene7 Image Serving - Image Rendering API
uuid: 81069578-8470-4ec0-b755-47b0a8124024
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 5%

---


# 앵커{#anchor}

이미지 앵커. 이 이미지가 템플릿 또는 합성 이미지에서 레이어로 사용될 경우 원점을 나타냅니다.

또한 회전의 기본 중심점을 정의합니다.

## 속성 {#section-95740f14160744e7bc763094b8be40d8}

2개의 정수(쉼표로 구분) 전체 해상도 이미지의 왼쪽 위 모서리를 기준으로 한 픽셀 오프셋입니다.

`anchor=`에 의해 재정의됨(`origin=`로 재정의할 수 있음).

## 기본값 {#section-ca3a4cc837d643519eff15951f2b47a1}

이 필드가 없거나 비어 있는 경우 이미지의 중심점이 사용되며, 이 필드가 유효한 이미지 레코드인 경우(즉, `catalog::Path`이 유효한 경우) 사용됩니다.

## 참조 {#section-f605d29c3f5d48ad8e2a374f11886f19}

[anchor=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) ,  [origin=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
