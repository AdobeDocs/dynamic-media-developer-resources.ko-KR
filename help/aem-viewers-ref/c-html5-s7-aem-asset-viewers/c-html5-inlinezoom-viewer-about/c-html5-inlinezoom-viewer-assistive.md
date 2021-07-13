---
description: 모든 뷰어 구성 요소는 화면 판독기와 같은 보조 기술과의 통합을 개선하기 위해 ARIA(Accessible Rich Internet Applications) 역할 및 속성을 지원합니다.
solution: Experience Manager
title: 보조 기술 지원
feature: Dynamic Media Classic,Viewers,SDK/API,인라인 확대/축소,접근성
role: Developer,User
exl-id: 8aa88456-b78b-434b-a98f-effce83ccd21
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---

# 보조 기술 지원{#assistive-technology-support}

모든 뷰어 구성 요소는 화면 판독기와 같은 보조 기술과의 통합을 개선하기 위해 ARIA(Accessible Rich Internet Applications) 역할 및 속성을 지원합니다.

최상위 뷰어 요소에는 기본적으로 뷰어 이름으로 설정된 역할 `region` 및 `aria-label` 특성이 있습니다. `Container.LABEL` 현지화 기호를 사용하여 레이블을 제어할 수 있습니다.

기본 보기에는 `application` 역할이 있습니다. 기본 보기에 대한 간단한 설명은 `aria-roledescription`에 있으며, 해당 기본 보기 구성 요소의 `ROLE_DESCRIPTION` 현지화 심볼에 정의된 값이 있습니다. 키보드 사용자에 대한 탐색 힌트는 `aria-describedby`을 사용하여 제공되며, 사용 힌트의 텍스트는 `USAGE_HINT` 현지화 심볼에서 가져옵니다. 자산에 UserData 필드에 정의된 레이블이 있는 경우 `aria-label` 속성은 해당 레이블 값으로 설정됩니다.

견본을 표시하는 구성 요소에는 `aria-label` 속성이 해당 구성 요소의 `LABEL` 현지화 기호 값으로 설정된 역할 `listbox`이 있습니다. 개별 색상 견본은 `aria-setsize` 및 `aria-posinset` 특성이 있는 `option` 역할을 가지고 세트에서 견본 위치를 설명합니다. 견본을 선택하면 `aria-selected` 속성이 `true`로 설정됩니다.
