---
description: 모든 뷰어 구성 요소는 ARIA(Accessible Rich Internet Application) 역할 및 속성을 지원하여 화면 판독기와 같은 보조 기술과의 통합을 향상시킵니다.
seo-description: 모든 뷰어 구성 요소는 ARIA(Accessible Rich Internet Application) 역할 및 속성을 지원하여 화면 판독기와 같은 보조 기술과의 통합을 향상시킵니다.
seo-title: 보조 기술 지원
solution: Experience Manager
title: 보조 기술 지원
topic: Dynamic media
uuid: 525ab400-c022-4f33-a0e3-bafb6019f1a7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---


# 보조 기술 지원{#assistive-technology-support}

모든 뷰어 구성 요소는 ARIA(Accessible Rich Internet Application) 역할 및 속성을 지원하여 화면 판독기와 같은 보조 기술과의 통합을 향상시킵니다.

최상위 수준 뷰어 요소에는 기본적으로 뷰어 이름으로 설정된 역할 `region` 및 `aria-label` 특성이 있습니다. `Container.LABEL` 현지화 기호를 사용하여 레이블을 제어할 수 있습니다.

단추에는 `button` 역할과 `aria-label` 특성이 있는 설명 텍스트 세트가 있습니다. `aria-label` 속성 값은 단추의 현지화 기호 값에서 채워집니다. 단추가 비활성화되면 `aria-disabled` 특성이 그에 따라 설정됩니다.

기본 보기에는 `application` 역할이 있습니다. 기본 보기에 대한 간단한 설명은 해당 기본 보기 구성 요소의 `ROLE_DESCRIPTION` 현지화 심볼에 의해 정의된 값과 함께 `aria-roledescription`에 제공됩니다. 키보드 사용자에 대한 탐색 힌트는 `aria-describedby`을(를) 사용하여 제공되지만 사용 힌트에 대한 텍스트는 `USAGE_HINT` 현지화 심볼에서 제공됩니다. 자산에 UserData 필드에 정의된 레이블이 있는 경우 `aria-label` 속성은 해당 레이블의 값으로 설정됩니다.

핫 스팟, 지역 및 이미지 맵은 핫 스팟 또는 이미지 맵 레이블의 값을 사용하여 `button` 역할과 `aria-label` 특성을 가진 설명 텍스트 세트를 사용합니다. 사용자가 핫 스팟 또는 이미지 맵에 초점을 맞출 때 키보드 사용자에 대한 탐색 힌트는 `aria-describedby`을(를) 사용하여 제공되며 사용 힌트에 대한 텍스트는 `USAGE_HINT` 현지화 심볼에서 제공됩니다.

축소판에는 `ThumbnailGridView.LABEL` 현지화 심볼에서 `aria-label` 특성을 제어하는 `dialog` 역할이 있습니다. 개별 축소판에는 `button` 역할이 있습니다. 축소판을 선택하면 `aria-selected` 속성이 `true`로 설정됩니다.

견본을 표시하는 구성 요소에는 `aria-label` 특성이 해당 구성 요소의 `LABEL` 현지화 기호 값으로 설정된 `listbox` 역할이 있습니다. 개별 색상 견본에는 세트의 견본 위치를 설명하는 `aria-setsize` 및 `aria-posinset` 특성이 있는 `option` 역할이 있습니다. 견본을 선택하면 `aria-selected` 속성이 `true`로 설정됩니다.

드롭다운 목록은 추가 `aria-haspopup` 특성이 `true`로 설정된 버튼과 실제 드롭다운 패널 요소를 참조하는 `aria-controls` 특성이 있는 버튼에 의해 활성화됩니다. 드롭다운 패널에는 `menuitem` 역할을 가진 하위 요소가 있는 `menu` 역할이 있습니다. 각 메뉴 항목에는 `aria-label` 특성이 지정되어 있습니다.

검색 사용자 인터페이스는 `search` 역할이 있는 요소로 그룹화됩니다. 검색 입력 필드에는 `searchbox` 역할이 있으며 `aria-describedby` 특성이 있는 `SearchPanel.INFO_PROMPT` 현지화 기호로 제어되는 정보 레이블을 참조합니다.

모달 대화 상자에는 `dialog` 역할이 있습니다. 대화 상자의 헤더 요소는 `aria-labelledby` 속성에서 참조됩니다.
