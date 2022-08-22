---
title: TiffEncoding
description: TIFF 인코딩 형식입니다. TIFF 이미지의 압축 형식을 지정합니다. fmt= 명령의 세 번째 값에 대한 기본값은 효과적입니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6a6fa8f5-4497-438d-914c-3f6d4c08ef09
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 5%

---

# TiffEncoding{#tiffencoding}

TIFF 인코딩 형식입니다. TIFF 이미지의 압축 형식을 지정합니다. 기본값은 의 세 번째 값에 적용됩니다 `fmt=` 명령).

을 로 설정합니다. `0` 압축이 없는 경우 `1` LZW용, `2` deflate(ZIP) 및 `3` JPEG 압축용.

## 속성 {#section-469f5a1225464542866f5353edd92db3}

열거형.

## 기본값 {#section-a3c5152a9f464e4987ed7c05d35b1169}

상속됨 `default::TiffEncoding` 정의되지 않았거나 비어 있는 경우.

## 참조 {#section-1601425e5ac3486da4df8e7fa55981b2}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)
