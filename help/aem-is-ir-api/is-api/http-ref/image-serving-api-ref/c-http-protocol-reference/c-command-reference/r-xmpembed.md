---
description: XMP 메타데이터 포함. 응답 이미지에 XMP 메타데이터를 포함할지 여부를 지정합니다.
solution: Experience Manager
title: xmpEmbed
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 353b6ac4-1141-4f17-a3ad-ad48b321b36f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---

# xmpEmbed{#xmpembed}

XMP 메타데이터 포함. 응답 이미지에 XMP 메타데이터를 포함할지 여부를 지정합니다.

`xmpEmbed=0|1`

>[!NOTE]
>
>XMP 데이터는 수정 없이 소스 이미지에서 응답 이미지로 전달됩니다. 이로 인해 응답 이미지에 잘못된 데이터가 포함될 수 있습니다.

## 속성 {#section-27024c4272f44d9a8c264a0629193af2}

요청 속성입니다. 소스 이미지에 XMP 데이터가 포함되어 있지 않으면 무시됩니다. `layer=0` 소스 이미지의 XMP 데이터만 처리됩니다. 다른 레이어 이미지의 XMP 데이터는 무시됩니다.

출력 이미지 형식이 XMP 포함을 지원하지 않는 경우에는 무시됩니다. XMP 포함 기능을 지원하는 출력 이미지 형식 목록은 `fmt=`에 대한 설명을 참조하십시오.

## 기본값 {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`를 사용하도록 선택할 수 있습니다.

## 참조 {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
