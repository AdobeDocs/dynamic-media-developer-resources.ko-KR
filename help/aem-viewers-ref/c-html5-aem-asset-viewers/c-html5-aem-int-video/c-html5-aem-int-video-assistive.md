---
title: 보조 기술 지원
description: 모든 뷰어 구성 요소는 ARIA(Accessible Rich Internet Applications) 역할 및 속성을 지원하여 화면 판독기와 같은 보조 기술과의 통합을 향상시킵니다.
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

모든 뷰어 구성 요소는 ARIA(Accessible Rich Internet Applications) 역할 및 속성을 지원하여 화면 판독기와 같은 보조 기술과의 통합을 향상시킵니다.

최상위 뷰어 요소에 역할이 있음 `region` 및 `aria-label` 속성이 기본적으로 뷰어의 이름으로 설정됩니다. 다음을 사용하여 레이블을 제어할 수 있습니다. `Container.LABEL` 지역화 기호.

단추에 역할 있음 `button` 및 설명 텍스트 세트 `aria-label` 특성. 값: `aria-label` 속성은 버튼의 현지화 기호 값에서 채워집니다. 버튼이 비활성화되면 `aria-disabled` 속성이 적절하게 설정됩니다.

슬라이더 구성 요소에 역할 있음 `slider` 속성 포함 `aria-valuenow`, `aria-valuemin`, 및 `aria-valuemax` 현재 슬라이더 위치를 설명합니다.

썸네일에는 역할이 있습니다. `dialog` 포함 `aria-label` 에 의해 제어되는 속성 `ThumbnailGridView.LABEL` 지역화 기호. 개별 썸네일에는 역할이 있습니다. `button`. 썸네일을 선택하면 `aria-selected` 속성이 로 설정됨 `true`.

견본을 표시하는 구성 요소에는 역할이 있습니다 `listbox` 포함 `aria-label` 속성이 의 값으로 설정됨 `LABEL` 해당 구성 요소의 현지화 기호. 개별 색상 견본에는 역할이 있습니다 `option` 포함 `aria-setsize` 및 `aria-posinset` 세트의 견본 위치를 설명하는 속성입니다. 견본을 선택하면 `aria-selected` 속성이 로 설정됨 `true`.

드롭다운 목록은 추가 기능이 있는 버튼에 의해 활성화됩니다 `aria-haspopup` 속성이 로 설정됨 `true` 및 `aria-controls` 실제 드롭다운 패널 요소를 참조하는 속성입니다. 드롭다운 패널 자체에는 역할이 있습니다 `menu` 역할을 가진 하위 요소 포함 `menuitem`. 각 메뉴 항목에는 `aria-label` 특성을 지정했습니다.

모달 대화 상자에는 역할이 있습니다 `dialog`. 대화 상자의 헤더 요소를 `aria-labelledby` 특성.
