---
title: 자료
description: 이미지 렌더링은 비네팅의 그룹이나 개체에 재료를 적용합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fe5445e-de85-4f0c-8008-7716226ff966
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# 자료{#materials}

이미지 렌더링은 비네팅의 그룹이나 개체에 재료를 적용합니다.

자료는 *특성* 집합으로 구성됩니다. 일부 속성은 특정 재료에 필요하며, 다른 속성은 선택 사항이며, 일부 속성은 존재하는 경우 무시됩니다. 많은 속성에는 기본값이 있습니다. 모든 물체에 모든 재료를 적용할 수 있는 것은 아닙니다(예: 소파에 캐비닛 재료를 적용할 수 없음).

MSS(Material Specification Segment) 내에서 발생하지만 위 또는 아래의 특정 자재 테이블에 나열되지 않은 모든 속성은 서버에서 무시됩니다.

다음 표에는 기본 재료 속성이 나열되어 있습니다. IR에서는 [고급 렌더링 효과](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281)를 제어하기 위한 추가 특성을 지원합니다.

별도로 언급되지 않는 한, 모든 재료 속성은 적절한 기본값을 갖는 선택 사항입니다.

* [단색](r-ir-solid-colors.md)
* [반복 가능한 텍스처](r-ir-repeatable-textures.md)
* [벽 테두리](r-ir-wall-borders.md)
* [데칼](r-ir-decals.md)
* [캐비닛](r-ir-cabinets.md)
* [창 커버링](r-ir-window-coverings.md)
