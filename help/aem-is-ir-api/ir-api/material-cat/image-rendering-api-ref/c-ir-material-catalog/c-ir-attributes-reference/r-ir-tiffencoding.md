---
title: Tiff 인코딩
description: TIFF 인코딩 형식입니다. TIFF 이미지의 압축 형식을 지정합니다(fmt= 명령의 세 번째 값에 대해 사실상 기본값).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6a6fa8f5-4497-438d-914c-3f6d4c08ef09
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 4%

---

# Tiff 인코딩{#tiffencoding}

TIFF 인코딩 형식입니다. TIFF 이미지의 압축 형식을 지정합니다(`fmt=` 명령의 세 번째 값에 대한 기본값).

압축을 사용하지 않으려면 `0`, LZW의 경우 `1`, ZIP(수축)의 경우 `2`, JPEG 압축의 경우 `3`(으)로 설정합니다.

## 속성 {#section-469f5a1225464542866f5353edd92db3}

열거형.

## 기본값 {#section-a3c5152a9f464e4987ed7c05d35b1169}

정의되지 않았거나 비어 있는 경우 `default::TiffEncoding`에서 상속됩니다.

## 참조 {#section-1601425e5ac3486da4df8e7fa55981b2}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)
