---
description: 레이어= 명령으로 지정한 순서대로 합성됩니다. 레이어 번호가 높은 레이어는 번호가 낮은 레이어를 숨깁니다.
seo-description: 레이어= 명령으로 지정한 순서대로 합성됩니다. 레이어 번호가 높은 레이어는 번호가 낮은 레이어를 숨깁니다.
seo-title: 합성 캔버스
solution: Experience Manager
title: 합성 캔버스
topic: Scene7 Image Serving - Image Rendering API
uuid: 057b11cb-36f3-40f8-b095-9ad05da858a9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 합성 캔버스{#the-compositing-canvas}

레이어= 명령으로 지정한 순서대로 합성됩니다. 레이어 번호가 높은 레이어는 번호가 낮은 레이어를 숨깁니다.

레이어 0은 배경 레이어를 구성하며 이는 항상 필요하고 합성 이미지의 크기를 정의합니다. 레이어 0에는 모든 레이어 유형이 허용됩니다. 레이어 0의 크기는 컨텐츠 이미지 또는 텍스트를 기반으로 명시적으로 `size=` 또는 암시적으로 정의해야 합니다. 레이어 0의 영역 밖에 있는 다른 레이어의 모든 영역은 출력 이미지에 포함되지 않습니다.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>모든 레이어가 병합된 후에는 [보기 명령 및 속성에](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90)지정된 대로 합성 이미지가 최종 응답 이미지로 변환됩니다.

