---
title: 보조 기술 지원
description: 모든 뷰어 구성 요소는 ARIA(Accessible Rich Internet Applications) 역할 및 속성을 지원하여 화면 판독기와 같은 보조 기술과의 통합을 향상시킵니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video,Accessibility
role: Developer,User
exl-id: e0652730-60ee-41db-890b-e223b279e47d
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# 보조 기술 지원{#assistive-technology-support}

모든 뷰어 구성 요소는 ARIA(Accessible Rich Internet Applications) 역할 및 속성을 지원하여 화면 판독기와 같은 보조 기술과의 통합을 향상시킵니다.

최상위 뷰어 요소에 역할이 있음 `region` 및 `aria-label` 속성이 기본적으로 뷰어의 이름으로 설정됩니다. 다음을 사용하여 레이블을 제어할 수 있습니다. `Container.LABEL` 지역화 기호.

단추에 역할 있음 `button` 및 설명 텍스트 세트 `aria-label` 특성. 값: `aria-label` 속성은 버튼의 현지화 기호 값에서 채워집니다. 버튼이 비활성화되면 `aria-disabled` 속성이 적절하게 설정됩니다.

슬라이더 구성 요소에 역할 있음 `slider` 속성 포함 `aria-valuenow`, `aria-valuemin`, 및 `aria-valuemax` 현재 슬라이더 위치를 설명합니다.

드롭다운 목록은 추가 기능이 있는 버튼에 의해 활성화됩니다 `aria-haspopup` 속성이 로 설정됨 `true` 및 `aria-controls` 실제 드롭다운 패널 요소를 참조하는 속성입니다. 드롭다운 패널 자체에는 역할이 있습니다 `menu` 역할을 가진 하위 요소 포함 `menuitem`. 각 메뉴 항목에는 `aria-label` 특성을 지정했습니다.

모달 대화 상자에는 역할이 있습니다 `dialog`. 대화 상자의 헤더 요소를 `aria-labelledby` 특성.
