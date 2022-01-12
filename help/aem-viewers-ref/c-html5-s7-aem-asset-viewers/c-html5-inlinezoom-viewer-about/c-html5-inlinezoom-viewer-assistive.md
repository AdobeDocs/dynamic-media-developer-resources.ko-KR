---
title: 보조 기술 지원
description: 모든 뷰어 구성 요소는 화면 판독기와 같은 보조 기술과의 통합을 개선하기 위해 ARIA(Accessible Rich Internet Applications) 역할 및 속성을 지원합니다.
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

모든 뷰어 구성 요소는 화면 판독기와 같은 보조 기술과의 통합을 개선하기 위해 ARIA(Accessible Rich Internet Applications) 역할 및 속성을 지원합니다.

최상위 뷰어 요소에는 역할이 있습니다 `region` 및 `aria-label` 기본적으로 설정된 속성은 뷰어 이름으로 설정됩니다. 를 사용하여 레이블을 제어할 수 있습니다 `Container.LABEL` 로컬라이제이션 기호

기본 보기에는 역할이 있습니다 `application`. 기본 보기에 대한 간단한 설명은 `aria-roledescription`에 정의된 값을 사용하여 `ROLE_DESCRIPTION` 해당 기본 보기 구성 요소의 로컬라이제이션 기호 키보드 사용자에 대한 탐색 힌트는 `aria-describedby`를 설정하는 경우 사용 힌트의 텍스트는 `USAGE_HINT` 로컬라이제이션 기호 자산에 UserData 필드에 정의된 레이블이 있는 경우 `aria-label` 속성이 해당 레이블의 값으로 설정되어 있습니다.

색상 견본을 표시하는 구성 요소가 역할을 합니다 `listbox` with `aria-label` 속성이 `LABEL` 해당 구성 요소의 로컬라이제이션 기호 개별 색상 견본에는 역할이 있습니다 `option` with `aria-setsize` 및 `aria-posinset` 세트에서 견본 위치를 설명하는 속성입니다. 견본을 선택하면 `aria-selected` 속성 설정 `true`.
