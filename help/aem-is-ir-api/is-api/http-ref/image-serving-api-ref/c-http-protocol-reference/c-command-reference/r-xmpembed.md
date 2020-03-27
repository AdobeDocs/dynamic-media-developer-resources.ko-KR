---
description: XMP 메타데이터 포함 XMP 메타데이터를 응답 이미지에 포함할지 여부를 지정합니다.
seo-description: XMP 메타데이터 포함 XMP 메타데이터를 응답 이미지에 포함할지 여부를 지정합니다.
seo-title: xmpEmbed
solution: Experience Manager
title: xmpEmbed
topic: Scene7 Image Serving - Image Rendering API
uuid: c0dfd0e5-16d1-4a6e-957a-ecc276b9361a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# xmpEmbed{#xmpembed}

XMP 메타데이터 포함 XMP 메타데이터를 응답 이미지에 포함할지 여부를 지정합니다.

`xmpEmbed=0|1`

>[!NOTE]
>
>XMP 데이터는 수정 없이 소스 이미지에서 응답 이미지로 전달됩니다. 이로 인해 응답 이미지에 잘못된 데이터가 포함될 수 있습니다.

## 속성 {#section-27024c4272f44d9a8c264a0629193af2}

요청 속성입니다. 소스 이미지에 XMP 데이터가 포함되어 있지 않으면 무시됩니다. 의 소스 이미지의 XMP 데이터만 `layer=0` 처리됩니다. 다른 레이어 이미지의 XMP 데이터는 무시됩니다.

출력 이미지 형식이 XMP 임베딩을 지원하지 않는 경우 무시됩니다. XMP 임베딩을 지원하는 출력 이미지 형식 목록은 의 설명을 `fmt=` 참조하십시오.

## 기본값 {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`를 사용하여 출력 이미지에 패스를 임베드할 수 없습니다.

## 참조 {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
