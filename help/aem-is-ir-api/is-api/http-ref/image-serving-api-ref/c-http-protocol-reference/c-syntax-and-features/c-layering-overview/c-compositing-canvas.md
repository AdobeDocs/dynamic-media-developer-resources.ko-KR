---
description: 레이어는 layer= 명령에 지정된 순서대로 합성됩니다. 여기서 번호가 높은 레이어는 번호가 낮은 레이어를 숨깁니다.
solution: Experience Manager
title: 합성 캔버스
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2455d07f-a158-4335-a14c-213f8b3dd265
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# 합성 캔버스{#the-compositing-canvas}

레이어는 layer= 명령에 지정된 순서대로 합성됩니다. 여기서 번호가 높은 레이어는 번호가 낮은 레이어를 숨깁니다.

레이어 0은 항상 필요하고 합성 이미지의 크기를 정의하는 배경 레이어를 구성합니다. 레이어 0에는 모든 레이어 유형이 허용됩니다. 레이어 0의 크기는 `size=`을(를) 명시적으로 사용하거나 콘텐츠 이미지 또는 텍스트를 기반으로 암묵적으로 정의해야 합니다. 레이어 0의 영역 밖에 있는 다른 레이어의 영역은 출력 이미지에 포함되지 않습니다.

>[!NOTE]
>
>모든 레이어가 병합되면 [보기 명령 및 특성](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90)에 지정된 대로 합성 이미지가 최종 응답 이미지로 변환됩니다.
