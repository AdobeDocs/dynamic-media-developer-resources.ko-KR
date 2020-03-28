---
description: 모든 뷰어 구성 요소는 화면 판독기와 같은 보조 기술과의 통합을 개선하기 위해 ARIA(액세스 가능한 리치 인터넷 애플리케이션) 역할 및 속성을 지원합니다.
seo-description: 모든 뷰어 구성 요소는 화면 판독기와 같은 보조 기술과의 통합을 개선하기 위해 ARIA(액세스 가능한 리치 인터넷 애플리케이션) 역할 및 속성을 지원합니다.
seo-title: 보조 기술 지원
solution: Experience Manager
title: 보조 기술 지원
topic: Dynamic media
uuid: 0abed8d4-9754-47b1-9de7-cce665de03b4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 보조 기술 지원{#assistive-technology-support}

모든 뷰어 구성 요소는 화면 판독기와 같은 보조 기술과의 통합을 개선하기 위해 ARIA(액세스 가능한 리치 인터넷 애플리케이션) 역할 및 속성을 지원합니다.

최상위 뷰어 요소에는 기본적으로 뷰어 이름으로 설정된 역할 `region` 및 `aria-label` 속성이 있습니다. 현지화 기호로 레이블을 제어할 수 `Container.LABEL` 있습니다.

단추에는 `button` 특성이 있는 역할 `aria-label` 및 설명 텍스트 세트가 있습니다. 속성의 값은 단추의 현지화 기호 값에서 채워집니다. `aria-label` 단추가 비활성화되면 `aria-disabled` 속성이 적절하게 설정됩니다.

슬라이더 구성 요소에는 `slider` 속성 `aria-valuenow`및 현재 슬라이더 위치를 설명하는 역할이 `aria-valuemin``aria-valuemax` 있습니다.

축소판에는 `dialog` 현지화 기호로 제어되는 `aria-label` `ThumbnailGridView.LABEL` 특성이 있습니다. 개별 축소판에는 역할이 `button`있습니다. 축소판을 선택하면 `aria-selected` 속성이 로 설정됩니다 `true`.

견본을 표시하는 구성 요소에는 해당 구성 요소의 현지화 기호 값으로 `listbox` 설정된 `aria-label` `LABEL` 속성이 있습니다. 개별 견본은 세트에서 견본 위치를 설명하는 `option` 속성 `aria-setsize` 및 `aria-posinset` 함께 역할을 합니다. 견본을 선택하면 `aria-selected` 속성 세트가 로 설정됩니다 `true`.

드롭다운 목록은 추가 `aria-haspopup` 속성이 로 설정된 버튼과 실제 드롭다운 패널 요소를 참조하는 `true` `aria-controls` 속성이 있는 단추로 활성화됩니다. 드롭다운 패널 자체에는 하위 요소가 역할을 `menu` 가지는 역할이 `menuitem`있습니다. 각 메뉴 항목에 지정된 `aria-label` 속성이 있습니다.

모달 대화 상자에는 역할이 `dialog`있습니다. 대화 상자의 헤더 요소는 `aria-labelledby` 속성에서 참조합니다.
