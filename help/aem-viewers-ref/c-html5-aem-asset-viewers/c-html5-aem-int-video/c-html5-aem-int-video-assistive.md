---
title: 보조 기술 지원
description: 모든 뷰어 구성 요소는 화면 판독기와 같은 보조 기술과의 통합을 개선하기 위해 ARIA(Accessible Rich Internet Applications) 역할 및 속성을 지원합니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos,Accessibility
role: Developer,User
exl-id: 3d9f6389-e73c-4d31-a7c1-b321f065ce8c
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# 보조 기술 지원{#assistive-technology-support}

모든 뷰어 구성 요소는 화면 판독기와 같은 보조 기술과의 통합을 개선하기 위해 ARIA(Accessible Rich Internet Applications) 역할 및 속성을 지원합니다.

최상위 뷰어 요소에는 기본적으로 뷰어 이름으로 설정된 역할 `region` 및 `aria-label` 특성이 있습니다. `Container.LABEL` 현지화 기호를 사용하여 레이블을 제어할 수 있습니다.

단추에는 `button` 역할과 `aria-label` 특성이 있는 설명 텍스트 세트가 있습니다. `aria-label` 속성 값은 단추의 현지화 기호 값에서 채워집니다. 단추가 비활성화되면 `aria-disabled` 속성이 그에 따라 설정됩니다.

슬라이더 구성 요소에는 현재 슬라이더 위치를 설명하는 `aria-valuenow`, `aria-valuemin` 및 `aria-valuemax` 특성이 있는 `slider` 역할이 있습니다.

미리 보기에는 `ThumbnailGridView.LABEL` 지역화 기호로 제어되는 `aria-label` 특성이 있는 `dialog` 역할이 있습니다. 개별 미리 보기에는 `button` 역할이 있습니다. 축소판을 선택하면 `aria-selected` 속성이 `true`로 설정됩니다.

견본을 표시하는 구성 요소에는 `aria-label` 속성이 해당 구성 요소의 `LABEL` 현지화 기호 값으로 설정된 역할 `listbox`이 있습니다. 개별 색상 견본은 `aria-setsize` 및 `aria-posinset` 특성이 있는 `option` 역할을 가지고 세트에서 견본 위치를 설명합니다. 견본을 선택하면 `aria-selected` 속성이 `true`로 설정됩니다.

드롭다운 목록은 추가 `aria-haspopup` 속성이 `true` 로 설정되고 실제 드롭다운 패널 요소를 참조하는 `aria-controls` 특성이 있는 단추에 의해 활성화됩니다. 드롭다운 패널 자체에는 `menuitem` 역할을 가진 하위 요소가 있는 `menu` 역할이 있습니다. 각 메뉴 항목에 `aria-label` 특성이 지정되어 있습니다.

모달 대화 상자에는 `dialog` 역할이 있습니다. 대화 상자의 헤더 요소는 `aria-labelledby` 특성에 의해 참조됩니다.
