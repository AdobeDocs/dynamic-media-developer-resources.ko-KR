---
description: 모든 뷰어 구성 요소는 ARIA(Accessible Rich Internet Applications) 역할 및 속성을 지원하여 화면 판독기와 같은 보조 기술과의 통합을 향상시킵니다.
solution: Experience Manager
title: 보조 기술 지원
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search,Accessibility
role: Developer,User
exl-id: fbfc9415-6ab8-466c-9a1f-d33565eff2a4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# 보조 기술 지원{#assistive-technology-support}

모든 뷰어 구성 요소는 ARIA(Accessible Rich Internet Applications) 역할 및 속성을 지원하여 화면 판독기와 같은 보조 기술과의 통합을 향상시킵니다.

최상위 뷰어 요소에 역할이 있음 `region` 및 `aria-label` 속성이 기본적으로 뷰어의 이름으로 설정됩니다. 다음을 사용하여 레이블을 제어할 수 있습니다. `Container.LABEL` 지역화 기호.

단추에 역할 있음 `button` 및 설명 텍스트 세트 `aria-label` 특성. 값: `aria-label` 속성은 버튼의 현지화 기호 값에서 채워집니다. 단추가 비활성화되면 `aria-disabled` 속성이 적절하게 설정됩니다.

기본 보기에 역할이 있습니다. `application`. 기본 보기에 대한 간략한 설명은에 제공됩니다. `aria-roledescription`로 정의된 값 사용 `ROLE_DESCRIPTION` 해당 기본 보기 구성 요소의 현지화 기호. 키보드 사용자를 위한 탐색 힌트는 `aria-describedby`, 사용 힌트의 텍스트는 `USAGE_HINT` 지역화 기호. 에셋에 UserData 필드에 정의된 레이블이 있는 경우 `aria-label` 속성은 이러한 레이블의 값으로 설정됩니다.

핫스팟, 영역 및 이미지 맵에는 역할이 있습니다 `button` 및 설명 텍스트 세트 `aria-label` 속성(핫스팟 또는 이미지 맵 레이블 값 포함) 사용자가 핫스팟 또는 이미지 맵에 초점을 맞추면 다음을 사용하여 키보드 사용자를 위한 탐색 힌트가 제공됩니다 `aria-describedby`에서 나오는 사용 힌트에 대한 텍스트가 있는 `USAGE_HINT` 지역화 기호.

썸네일에는 역할이 있습니다. `dialog` 포함 `aria-label` 에 의해 제어되는 속성 `ThumbnailGridView.LABEL` 지역화 기호. 개별 썸네일에는 역할이 있습니다. `button`. 썸네일을 선택하면 `aria-selected` 속성이 로 설정됨 `true`.

견본을 표시하는 구성 요소에는 역할이 있습니다 `listbox` 포함 `aria-label` 속성이 의 값으로 설정됨 `LABEL` 해당 구성 요소의 현지화 기호. 개별 색상 견본에는 역할이 있습니다 `option` 포함 `aria-setsize` 및 `aria-posinset` 세트의 견본 위치를 설명하는 속성입니다. 견본을 선택하면 `aria-selected` 속성이 로 설정됨 `true`.

드롭다운 목록은 추가 기능이 있는 버튼에 의해 활성화됩니다 `aria-haspopup` 속성이 로 설정됨 `true` 및 `aria-controls` 실제 드롭다운 패널 요소를 참조하는 속성입니다. 드롭다운 패널 자체에는 역할이 있습니다 `menu` 역할을 가진 하위 요소 포함 `menuitem`. 각 메뉴 항목에는 `aria-label` 특성을 지정했습니다.

검색 사용자 인터페이스는 역할이 있는 요소에 그룹화됩니다 `search`. 검색 입력 필드에 역할이 있음 `searchbox` 및 는에서 제어하는 정보 레이블을 참조합니다. `SearchPanel.INFO_PROMPT` 지역화 기호 `aria-describedby` 특성.

모달 대화 상자에는 역할이 있습니다 `dialog`. 대화 상자의 헤더 요소를 `aria-labelledby` 특성.
