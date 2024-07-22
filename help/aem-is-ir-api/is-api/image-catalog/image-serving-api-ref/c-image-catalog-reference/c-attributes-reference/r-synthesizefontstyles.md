---
title: 합성 글꼴 스타일
description: 합성 글꼴 변형을 사용합니다. 굵게, 기울임꼴 또는 굵은 기울임꼴 스타일이 요청되었지만 글꼴 맵에서 찾을 수 없는 경우 서버에서 오류 응답을 생성할지 또는 굵게, 기울임꼴 또는 굵은 기울임꼴 스타일을 합성할지 여부를 제어합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08f20748-71c7-4b9f-9b45-70352f9abf35
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 2%

---

# 합성 글꼴 스타일{#synthesizefontstyles}

합성 글꼴 변형을 사용합니다. 굵게, 기울임꼴 또는 굵은 기울임꼴 스타일이 요청되었지만 글꼴 맵에서 찾을 수 없는 경우 서버에서 오류 응답을 생성할지 또는 굵게, 기울임꼴 또는 굵은 기울임꼴 스타일을 합성할지 여부를 제어합니다.

>[!NOTE]
>
>글꼴 스타일을 합성하면 이러한 스타일에 실제 글꼴을 사용하는 것보다 품질 렌더링이 낮은 경우가 많습니다.

## 속성 {#section-3205560a74774ebf9c916b07bd15aca6}

플래그. 0으로 설정하면 비활성화되고 1로 설정하면 합성 글꼴 스타일이 활성화됩니다.

## 기본값 {#section-71f94aa65e404d14b441674c040b59e3}

정의되지 않았거나 비어 있는 경우 `default::SynthesizeFontStyles`에서 상속됩니다.

## 참조 {#section-47a79659cc844272b6d5f36c946e12ac}

[글꼴 맵 참조](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d)
