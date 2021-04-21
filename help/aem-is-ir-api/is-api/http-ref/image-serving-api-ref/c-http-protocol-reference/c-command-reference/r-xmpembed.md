---
description: XMP 메타데이터 포함. XMP 메타데이터를 응답 이미지에 포함할지 여부를 지정합니다.
solution: Experience Manager
title: xmpEmbed
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 2%

---


# xmpEmbed{#xmpembed}

XMP 메타데이터 포함. XMP 메타데이터를 응답 이미지에 포함할지 여부를 지정합니다.

`xmpEmbed=0|1`

>[!NOTE]
>
>XMP 데이터는 수정 없이 소스 이미지에서 응답 이미지로 전달됩니다. 이로 인해 잘못된 데이터가 응답 이미지에 포함될 수 있습니다.

## 속성 {#section-27024c4272f44d9a8c264a0629193af2}

요청 속성을 참조하십시오. 소스 이미지에 XMP 데이터가 포함되어 있지 않으면 무시됩니다. `layer=0`의 소스 이미지의 XMP 데이터만 처리됩니다. 다른 레이어 이미지의 XMP 데이터는 무시됩니다.

출력 이미지 형식이 XMP 임베딩을 지원하지 않는 경우 무시됩니다. XMP 임베딩을 지원하는 출력 이미지 형식 목록은 `fmt=` 설명을 참조하십시오.

## 기본값 {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`를 선택합니다.

## 참조 {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
