---
title: 보조 기술 지원
description: 모든 뷰어 구성 요소는 화면 판독기와 같은 보조 기술과의 통합을 개선하기 위해 ARIA(Accessible Rich Internet Applications) 역할 및 속성을 지원합니다.
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

모든 뷰어 구성 요소는 화면 판독기와 같은 보조 기술과의 통합을 개선하기 위해 ARIA(Accessible Rich Internet Applications) 역할 및 속성을 지원합니다.

최상위 뷰어 요소에는 역할이 있습니다 `region` 및 `aria-label` 기본적으로 설정된 속성은 뷰어 이름으로 설정됩니다. 를 사용하여 레이블을 제어할 수 있습니다 `Container.LABEL` 로컬라이제이션 기호

버튼에는 역할이 있습니다 `button` 및 `aria-label` 속성을 사용합니다. 다음 값 `aria-label` 속성은 단추의 현지화 기호 값에서 채워집니다. 단추가 비활성화되면 `aria-disabled` 속성이 그에 따라 설정됩니다.

기본 보기에는 역할이 있습니다 `application`. 기본 보기에 대한 간단한 설명은 `aria-roledescription`에 정의된 값을 사용하여 `ROLE_DESCRIPTION` 해당 기본 보기 구성 요소의 로컬라이제이션 기호 키보드 사용자에 대한 탐색 힌트는 `aria-describedby`를 설정하는 경우 사용 힌트의 텍스트는 `USAGE_HINT` 로컬라이제이션 기호 자산에 UserData 필드에 정의된 레이블이 있는 경우 `aria-label` 속성이 해당 레이블의 값으로 설정되어 있습니다.

핫 스팟, 지역, 이미지 맵이 역할을 합니다 `button` 및 설명 텍스트 세트 `aria-label` 속성을 사용합니다. 사용자가 핫 스팟 또는 이미지 맵에 중점을 두면 키보드 사용자에 대한 탐색 힌트가 `aria-describedby`를 사용 힌트에 대한 텍스트는 `USAGE_HINT` 로컬라이제이션 기호

미리 보기에 역할이 있습니다. `dialog` with `aria-label` 에 의해 제어되는 속성 `ThumbnailGridView.LABEL` 로컬라이제이션 기호 개별 미리 보기에 역할이 있습니다. `button`. 축소판을 선택하면 축소판이 표시됩니다 `aria-selected` 속성 설정 `true`.

색상 견본을 표시하는 구성 요소가 역할을 합니다 `listbox` with `aria-label` 속성이 `LABEL` 해당 구성 요소의 로컬라이제이션 기호 개별 색상 견본에는 역할이 있습니다 `option` with `aria-setsize` 및 `aria-posinset` 세트에서 견본 위치를 설명하는 속성입니다. 견본을 선택하면 `aria-selected` 속성 설정 `true`.

드롭다운 목록은 추가 기능이 있는 단추에 의해 활성화됩니다 `aria-haspopup` 속성 설정 `true` 그리고 `aria-controls` 실제 드롭다운 패널 요소를 참조하는 속성입니다. 드롭다운 패널 자체에는 역할이 있습니다 `menu` 역할을 가진 하위 요소 사용 `menuitem`. 각 메뉴 항목에는 `aria-label` 속성을 지정했습니다.

모달 대화 상자에는 역할이 있습니다 `dialog`. 대화 상자의 헤더 요소는 `aria-labelledby` 속성을 사용합니다.
