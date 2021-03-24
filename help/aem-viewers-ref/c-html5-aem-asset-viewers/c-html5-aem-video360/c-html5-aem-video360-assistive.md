---
description: 모든 뷰어 구성 요소는 ARIA(Accessible Rich Internet Application) 역할 및 속성을 지원하여 화면 판독기와 같은 보조 기술과의 통합을 향상시킵니다.
solution: Experience Manager
title: 보조 기술 지원
feature: Dynamic Media Classic,뷰어,SDK/API,360 VR 비디오,접근성
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---


# 보조 기술 지원{#assistive-technology-support}

모든 뷰어 구성 요소는 ARIA(Accessible Rich Internet Application) 역할 및 속성을 지원하여 화면 판독기와 같은 보조 기술과의 통합을 향상시킵니다.

최상위 수준 뷰어 요소에는 기본적으로 뷰어 이름으로 설정된 역할 `region` 및 `aria-label` 특성이 있습니다. `Container.LABEL` 현지화 기호를 사용하여 레이블을 제어할 수 있습니다.

단추에는 `button` 역할과 `aria-label` 특성이 있는 설명 텍스트 집합이 있습니다. `aria-label` 속성 값은 단추의 현지화 기호 값에서 채워집니다. 단추가 비활성화되면 `aria-disabled` 특성이 그에 따라 설정됩니다.

슬라이더 구성 요소에는 현재 슬라이더 위치를 설명하는 `aria-valuenow`, `aria-valuemin` 및 `aria-valuemax` 특성이 있는 `slider` 역할이 있습니다.

드롭다운 목록은 실제 드롭다운 패널 요소를 참조하는 추가 `aria-haspopup` 속성이 `true` 및 `aria-controls` 속성으로 설정된 버튼에 의해 활성화됩니다. 드롭다운 패널에는 `menuitem` 역할을 가진 하위 요소가 있는 `menu` 역할이 있습니다. 각 메뉴 항목에는 `aria-label` 특성이 지정되어 있습니다.

모달 대화 상자에는 `dialog` 역할이 있습니다. 대화 상자의 헤더 요소는 `aria-labelledby` 속성에서 참조됩니다.
