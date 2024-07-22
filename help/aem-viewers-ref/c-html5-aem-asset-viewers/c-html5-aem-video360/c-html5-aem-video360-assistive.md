---
title: 보조 기술 지원
description: 모든 뷰어 구성 요소는 ARIA(Accessible Rich Internet Applications) 역할 및 속성을 지원하여 화면 판독기와 같은 보조 기술과의 통합을 향상시킵니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video,Accessibility
role: Developer,User
exl-id: 0d6bc444-a4c2-47e4-b408-a6df85ebff72
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# 보조 기술 지원{#assistive-technology-support}

모든 뷰어 구성 요소는 ARIA(Accessible Rich Internet Applications) 역할 및 속성을 지원하여 화면 판독기와 같은 보조 기술과의 통합을 향상시킵니다.

최상위 뷰어 요소에는 기본적으로 뷰어 이름으로 설정된 `region` 역할 및 `aria-label` 특성이 있습니다. `Container.LABEL` 지역화 기호를 사용하여 레이블을 제어할 수 있습니다.

단추에는 `aria-label` 특성이 있는 설명 텍스트 세트와 `button` 역할이 있습니다. `aria-label` 특성 값은 단추의 현지화 기호 값에서 채워집니다. 단추를 사용하지 않도록 설정하면 `aria-disabled` 특성이 그에 따라 설정됩니다.

슬라이더 구성 요소에는 현재 슬라이더 위치를 설명하는 `aria-valuenow`, `aria-valuemin` 및 `aria-valuemax` 특성이 있는 `slider` 역할이 있습니다.

추가 `aria-haspopup` 특성이 `true`(으)로 설정되어 있고 실제 드롭다운 패널 요소를 참조하는 `aria-controls` 특성이 있는 단추에 의해 드롭다운 목록이 활성화됩니다. 드롭다운 패널 자체에는 `menu` 역할이 있고 하위 요소에는 `menuitem` 역할이 있습니다. 각 메뉴 항목에는 `aria-label` 특성이 지정되어 있습니다.

모달 대화 상자에는 `dialog` 역할이 있습니다. 대화 상자의 헤더 요소를 `aria-labelledby` 특성에서 참조합니다.
