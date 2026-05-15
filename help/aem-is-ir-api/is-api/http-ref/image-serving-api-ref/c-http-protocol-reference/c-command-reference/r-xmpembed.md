---
title: xmpEmbed
description: XMP 메타데이터를 포함합니다. XMP 메타데이터를 응답 이미지에 포함할지 여부를 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 353b6ac4-1141-4f17-a3ad-ad48b321b36f
TQID: 'https://experienceleague.adobe.com/2pISbWU-Y-4szY0jmZswDIxvBrPlJ1yZmQby0sZ1v-o'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 126
ht-degree: 2%

---

# xmpEmbed{#xmpembed}

XMP 메타데이터를 포함합니다. XMP 메타데이터를 응답 이미지에 포함할지 여부를 지정합니다.

`xmpEmbed=0|1`

>[!NOTE]
>
>XMP 데이터는 수정하지 않고 소스 이미지에서 응답 이미지로 전달됩니다. 이로 인해 응답 이미지에 잘못된 데이터가 포함될 수 있습니다.

## 속성 {#section-27024c4272f44d9a8c264a0629193af2}

요청 속성입니다. 소스 이미지에 XMP 데이터가 포함되지 않은 경우 무시됩니다. `layer=0`의 원본 이미지에서 가져온 XMP 데이터만 처리됩니다. 다른 레이어 이미지의 XMP 데이터는 무시됩니다.

출력 이미지 형식이 XMP 포함을 지원하지 않는 경우에는 무시됩니다. XMP 포함을 지원하는 출력 이미지 형식 목록은 `fmt=`의 설명을 참조하십시오.

## 기본값 {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`(출력 이미지에 경로를 포함하지 않음)

## 참조 {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
