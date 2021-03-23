---
description: 모든 뷰어 구성 요소는 ARIA(Accessible Rich Internet Application) 역할 및 속성을 지원하여 화면 판독기와 같은 보조 기술과의 통합을 향상시킵니다.
seo-description: 모든 뷰어 구성 요소는 ARIA(Accessible Rich Internet Application) 역할 및 속성을 지원하여 화면 판독기와 같은 보조 기술과의 통합을 향상시킵니다.
seo-title: 보조 기술 지원
solution: Experience Manager
title: 보조 기술 지원
uuid: 9de323c9-d383-41e9-ae44-06600f44a85e
feature: Dynamic Media Classic,뷰어,SDK/API,인라인 확대/축소,접근성
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 0%

---


# 보조 기술 지원{#assistive-technology-support}

모든 뷰어 구성 요소는 ARIA(Accessible Rich Internet Application) 역할 및 속성을 지원하여 화면 판독기와 같은 보조 기술과의 통합을 향상시킵니다.

최상위 수준 뷰어 요소에는 기본적으로 뷰어 이름으로 설정된 역할 `region` 및 `aria-label` 특성이 있습니다. `Container.LABEL` 현지화 기호를 사용하여 레이블을 제어할 수 있습니다.

기본 보기에는 `application` 역할이 있습니다. 기본 보기에 대한 간단한 설명은 해당 기본 보기 구성 요소의 `ROLE_DESCRIPTION` 현지화 심볼에 의해 정의된 값과 함께 `aria-roledescription`에 제공됩니다. 키보드 사용자에 대한 탐색 힌트는 `aria-describedby`을(를) 사용하여 제공되지만 사용 힌트에 대한 텍스트는 `USAGE_HINT` 현지화 심볼에서 제공됩니다. 자산에 UserData 필드에 정의된 레이블이 있는 경우 `aria-label` 속성은 해당 레이블의 값으로 설정됩니다.

견본을 표시하는 구성 요소에는 `aria-label` 특성이 해당 구성 요소의 `LABEL` 현지화 기호 값으로 설정된 `listbox` 역할이 있습니다. 개별 색상 견본에는 세트의 견본 위치를 설명하는 `aria-setsize` 및 `aria-posinset` 특성이 있는 `option` 역할이 있습니다. 견본을 선택하면 `aria-selected` 속성이 `true`로 설정됩니다.
