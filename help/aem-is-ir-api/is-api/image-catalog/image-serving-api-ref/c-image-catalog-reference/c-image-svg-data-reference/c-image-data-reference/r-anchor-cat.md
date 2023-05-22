---
description: 이미지 앵커. 이 이미지를 템플릿이나 합성 이미지의 레이어로 사용할 때의 원점입니다.
solution: Experience Manager
title: 앵커
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c54b8bb2-af4f-4c05-be7b-4326dd08993a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 4%

---

# 앵커{#anchor}

이미지 앵커. 이 이미지를 템플릿이나 합성 이미지의 레이어로 사용할 때의 원점입니다.

또한 회전의 기본 중심점을 정의합니다.

## 속성 {#section-95740f14160744e7bc763094b8be40d8}

쉼표로 구분된 2개의 정수. 전체 해상도 이미지의 위쪽, 왼쪽 모서리를 기준으로 한 픽셀 오프셋입니다.

재정의한 사람 `anchor=`(다음으로 재정의할 수 있음) `origin=`).

## 기본값 {#section-ca3a4cc837d643519eff15951f2b47a1}

이 필드가 없거나 비어 있는 경우, 올바른 이미지 레코드인 경우(예: 인 경우) 이미지의 중심점이 사용됩니다. `catalog::Path` 은(는) 유효합니다.

## 참조 {#section-f605d29c3f5d48ad8e2a374f11886f19}

[앵커=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) , [origin=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
