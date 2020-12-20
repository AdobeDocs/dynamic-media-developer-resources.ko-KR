---
description: 이미지 렌더링은 비네팅의 그룹 또는 개체에 자료를 적용합니다.
seo-description: 이미지 렌더링은 비네팅의 그룹 또는 개체에 자료를 적용합니다.
seo-title: 자료
solution: Experience Manager
title: 자료
topic: Scene7 Image Serving - Image Rendering API
uuid: 82284e25-cfe0-4cf8-b410-b49196cc721c
translation-type: tm+mt
source-git-commit: 7721cccf3f779f258adcdcf886f7e01111e92be0
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---


# 자료{#materials}

이미지 렌더링은 비네팅의 그룹 또는 개체에 자료를 적용합니다.

자료는 *attributes* 세트로 구성됩니다. 일부 속성은 특정 자료에 필요하며, 다른 속성은 선택 사항이며, 일부 속성은 있을 경우 무시됩니다. 많은 속성에 기본값이 있습니다. 모든 개체에 모든 자료를 적용할 수 있는 것은 아닙니다(예: 캐비닛 자료는 소파에 적용할 수 없습니다).

MSS(Material Specification Segment) 내에서 발생하지만 위에 나열되거나 아래 특정 자료 테이블에 나열되지 않는 속성은 서버에서 무시됩니다.

다음 표에서는 기본 재료 속성을 나열합니다. IR는 [고급 렌더링 효과](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281)를 제어하기 위한 추가 속성을 지원합니다.

별도의 설명이 없는 한 모든 재료 속성은 적절한 기본값을 갖는 선택 사항입니다.

* [단색](r-ir-solid-colors.md)
* [반복 가능한 텍스처](r-ir-repeatable-textures.md)
* [벽 테두리](r-ir-wall-borders.md)
* [디칼스](r-ir-decals.md)
* [캐비닛](r-ir-cabinets.md)
* [윈도우 커버](r-ir-window-coverings.md)
