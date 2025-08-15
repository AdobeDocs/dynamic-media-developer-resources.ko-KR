---
title: 보조 기술 지원
description: 모든 뷰어 구성 요소는 ARIA(Accessible Rich Internet Applications) 역할 및 속성을 지원하여 화면 판독기와 같은 보조 기술과의 통합을 향상시킵니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog,Accessibility
role: Developer,User
exl-id: 46ccea4e-4314-453e-a987-68644467ab12
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# 보조 기술 지원{#assistive-technology-support}

모든 뷰어 구성 요소는 ARIA(Accessible Rich Internet Applications) 역할 및 속성을 지원하여 화면 판독기와 같은 보조 기술과의 통합을 향상시킵니다.

최상위 뷰어 요소에는 기본적으로 뷰어 이름으로 설정된 `region` 역할 및 `aria-label` 특성이 있습니다. `Container.LABEL` 지역화 기호를 사용하여 레이블을 제어할 수 있습니다.

단추에는 `button` 특성이 있는 설명 텍스트와 `aria-label` 역할이 설정되어 있습니다. `aria-label` 특성 값은 단추의 현지화 기호 값에서 채워집니다. 단추를 사용하지 않도록 설정하면 `aria-disabled` 특성이 그에 따라 설정됩니다.

기본 보기에 `application` 역할이 있습니다. 기본 보기에 대한 간략한 설명이 `aria-roledescription`에 제공됩니다. 이 값은 해당 기본 보기 구성 요소의 `ROLE_DESCRIPTION` 지역화 기호로 정의됩니다. `aria-describedby`을(를) 사용하여 키보드 사용자를 위한 탐색 힌트가 제공됩니다. 사용 힌트에 대한 텍스트는 `USAGE_HINT` 지역화 기호에서 가져옵니다. 에셋에 UserData 필드에 정의된 레이블이 있는 경우 `aria-label` 특성은 해당 레이블의 값으로 설정됩니다.

핫스팟, 지역 및 이미지 맵에는 `button` 역할이 있고 설명 텍스트가 핫스팟 또는 이미지 맵 레이블 값과 함께 `aria-label` 특성으로 설정되어 있습니다. 사용자가 핫스팟 또는 이미지 맵에 초점을 맞추면 `aria-describedby`을(를) 사용하여 키보드 사용자를 위한 탐색 힌트가 제공되며, 사용 힌트에 대한 텍스트는 `USAGE_HINT` 지역화 기호에서 가져옵니다.

썸네일에는 `dialog` 지역화 기호에 의해 제어되는 `aria-label` 특성을 가진 `ThumbnailGridView.LABEL` 역할이 있습니다. 개별 썸네일에는 `button` 역할이 있습니다. 썸네일을 선택하면 `aria-selected` 특성이 `true`(으)로 설정됩니다.

견본을 표시하는 구성 요소에 `listbox` 특성이 있는 `aria-label` 역할이 해당 구성 요소의 `LABEL` 지역화 기호 값으로 설정되어 있습니다. 개별 견본에는 집합의 견본 위치를 설명하는 `option` 및 `aria-setsize` 특성이 있는 `aria-posinset` 역할이 있습니다. 견본을 선택하면 `aria-selected` 특성이 `true`(으)로 설정됩니다.

드롭다운 목록은 추가 `aria-haspopup` 특성이 `true`(으)로 설정되어 있고 실제 드롭다운 패널 요소를 참조하는 `aria-controls` 특성이 있는 단추로 활성화됩니다. 드롭다운 패널 자체에는 `menu` 역할이 있고 하위 요소에는 `menuitem` 역할이 있습니다. 각 메뉴 항목에는 `aria-label` 특성이 지정되어 있습니다.

모달 대화 상자에는 `dialog` 역할이 있습니다. 대화 상자의 헤더 요소를 `aria-labelledby` 특성에서 참조합니다.
