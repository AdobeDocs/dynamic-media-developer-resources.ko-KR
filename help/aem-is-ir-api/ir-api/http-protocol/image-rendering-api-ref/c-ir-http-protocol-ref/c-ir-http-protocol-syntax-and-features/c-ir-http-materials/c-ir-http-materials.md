---
description: 이미지 렌더링은 비네팅의 그룹 또는 개체에 자료를 적용합니다.
solution: Experience Manager
title: 재료
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 3fe5445e-de85-4f0c-8008-7716226ff966
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# 재료{#materials}

이미지 렌더링은 비네팅의 그룹 또는 개체에 자료를 적용합니다.

자료는 *속성* 세트로 구성됩니다. 일부 속성은 특정 자료에 필요하며, 다른 속성은 선택 사항이며, 다른 속성은 있을 경우 무시됩니다. 많은 속성에 기본값이 있습니다. 모든 물체에 모든 재료를 적용할 수 있는 것은 아닙니다(예: 캐비닛 재료는 소파에 적용할 수 없음).

MSS(Material Specification Segment) 내에서 발생하지만 위에 나열되지 않고 아래 특정 자재 테이블에 나열되지 않은 속성은 서버에서 무시됩니다.

다음 표에는 기본 재료 속성이 나열되어 있습니다. IR은 [고급 렌더링 효과](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281)를 제어하기 위한 추가 속성을 지원합니다.

별도로 언급되지 않는 한 모든 재료 속성은 적절한 기본값을 사용하여 선택 사항입니다.

* [단색](r-ir-solid-colors.md)
* [반복 가능한 텍스처](r-ir-repeatable-textures.md)
* [벽 테두리](r-ir-wall-borders.md)
* [디칼](r-ir-decals.md)
* [캐비닛](r-ir-cabinets.md)
* [창문 커버](r-ir-window-coverings.md)
