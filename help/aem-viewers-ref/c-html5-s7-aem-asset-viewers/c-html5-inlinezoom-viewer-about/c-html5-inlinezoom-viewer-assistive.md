---
title: 보조 기술 지원
description: 모든 뷰어 구성 요소는 ARIA(Accessible Rich Internet Applications) 역할 및 속성을 지원하여 화면 판독기와 같은 보조 기술과의 통합을 향상시킵니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom,Accessibility
role: Developer,User
exl-id: 8aa88456-b78b-434b-a98f-effce83ccd21
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# 보조 기술 지원{#assistive-technology-support}

모든 뷰어 구성 요소는 ARIA(Accessible Rich Internet Applications) 역할 및 속성을 지원하여 화면 판독기와 같은 보조 기술과의 통합을 향상시킵니다.

최상위 뷰어 요소에는 기본적으로 뷰어 이름으로 설정된 `region` 역할 및 `aria-label` 특성이 있습니다. `Container.LABEL` 지역화 기호를 사용하여 레이블을 제어할 수 있습니다.

기본 보기에 `application` 역할이 있습니다. 기본 보기에 대한 간략한 설명이 `aria-roledescription`에 제공됩니다. 이 값은 해당 기본 보기 구성 요소의 `ROLE_DESCRIPTION` 지역화 기호로 정의됩니다. `aria-describedby`을(를) 사용하여 키보드 사용자를 위한 탐색 힌트가 제공됩니다. 사용 힌트에 대한 텍스트는 `USAGE_HINT` 지역화 기호에서 가져옵니다. 에셋에 UserData 필드에 정의된 레이블이 있는 경우 `aria-label` 특성은 해당 레이블의 값으로 설정됩니다.

견본을 표시하는 구성 요소에 `listbox` 특성이 있는 `aria-label` 역할이 해당 구성 요소의 `LABEL` 지역화 기호 값으로 설정되어 있습니다. 개별 견본에는 집합의 견본 위치를 설명하는 `option` 및 `aria-setsize` 특성이 있는 `aria-posinset` 역할이 있습니다. 견본을 선택하면 `aria-selected` 특성이 `true`(으)로 설정됩니다.
