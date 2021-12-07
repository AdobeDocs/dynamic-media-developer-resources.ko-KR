---
title: 보조 기술 지원
description: 모든 뷰어 구성 요소는 화면 판독기와 같은 보조 기술과의 통합을 개선하기 위해 ARIA(Accessible Rich Internet Applications) 역할 및 속성을 지원합니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video,Accessibility
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# 보조 기술 지원{#assistive-technology-support}

모든 뷰어 구성 요소는 화면 판독기와 같은 보조 기술과의 통합을 개선하기 위해 ARIA(Accessible Rich Internet Applications) 역할 및 속성을 지원합니다.

최상위 뷰어 요소에는 역할이 있습니다 `region` 및 `aria-label` 기본적으로 설정된 속성은 뷰어 이름으로 설정됩니다. 를 사용하여 레이블을 제어할 수 있습니다 `Container.LABEL` 로컬라이제이션 기호

버튼에는 역할이 있습니다 `button` 및 설명 텍스트 세트 `aria-label` 속성을 사용합니다. 다음 값 `aria-label` 속성은 단추의 현지화 기호 값에서 채워집니다. 단추가 비활성화되면 `aria-disabled` 속성이 그에 따라 설정됩니다.

슬라이더 구성 요소에는 역할이 있습니다 `slider` 속성 사용 `aria-valuenow`, `aria-valuemin`, 및 `aria-valuemax` 현재 슬라이더 위치를 설명합니다.

드롭다운 목록은 추가 기능이 있는 단추에 의해 활성화됩니다 `aria-haspopup` 속성 설정 `true` 및 `aria-controls` 실제 드롭다운 패널 요소를 참조하는 속성입니다. 드롭다운 패널 자체에는 역할이 있습니다 `menu` 역할을 가진 하위 요소 사용 `menuitem`. 각 메뉴 항목에는 `aria-label` 속성을 지정했습니다.

모달 대화 상자에는 역할이 있습니다 `dialog`. 대화 상자의 헤더 요소는 `aria-labelledby` 속성을 사용합니다.
