---
description: 이미지 앵커. 템플릿 또는 복합 이미지에서 레이어로 사용할 때의 원점.
solution: Experience Manager
title: 앵커
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c54b8bb2-af4f-4c05-be7b-4326dd08993a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 5%

---

# 앵커{#anchor}

이미지 앵커. 템플릿 또는 복합 이미지에서 레이어로 사용할 때의 원점.

또한 회전할 기본 중심점을 정의합니다.

## 속성 {#section-95740f14160744e7bc763094b8be40d8}

쉼표로 구분된 두 정수 숫자. 전체 해상도 이미지의 왼쪽 위 모서리에 대한 픽셀 오프셋입니다.

`anchor=`에 의해 재정의되며, 이 값은 `origin=`로 재정의할 수 있습니다.

## 기본값 {#section-ca3a4cc837d643519eff15951f2b47a1}

이 필드가 없거나 비어 있고 유효한 이미지 레코드인 경우(예: `catalog::Path` 이 유효한 경우) 이미지의 중심점이 사용됩니다.

## 참조 {#section-f605d29c3f5d48ad8e2a374f11886f19}

[anchor=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) ,  [origin=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
