---
title: 보조 기술 지원
description: 모든 뷰어 구성 요소는 화면 판독기와 같은 보조 기술과의 통합을 개선하기 위해 ARIA(Accessible Rich Internet Applications) 역할 및 속성을 지원합니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners,Accessibility
role: Developer,User
exl-id: 3ed943e8-4695-4561-9be0-1b6ed30294f8
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---

# 보조 기술 지원{#assistive-technology-support}

모든 뷰어 구성 요소는 화면 판독기와 같은 보조 기술과의 통합을 개선하기 위해 ARIA(Accessible Rich Internet Applications) 역할 및 속성을 지원합니다.

최상위 뷰어 요소에는 기본적으로 뷰어 이름으로 설정된 역할 `region` 및 `aria-label` 특성이 있습니다. `Container.LABEL` 현지화 기호를 사용하여 레이블을 제어할 수 있습니다.

단추에는 `button` 역할과 `aria-label` 특성이 있는 설명 텍스트 세트가 있습니다. `aria-label` 속성 값은 단추의 현지화 기호 값에서 채워집니다. 단추가 비활성화되면 `aria-disabled` 속성이 그에 따라 설정됩니다.

회전판 슬라이드를 탐색할 수 있는 버튼에는 현재 선택한 슬라이드에 따라 런타임 시 업데이트되는 레이블이 있습니다. 이러한 단추 레이블의 템플릿은 `CAROUSELVIEWER_TOOLTIP_GOTO` 지역화 심볼로 설정되어 있습니다.

기본 보기에는 `application` 역할이 있습니다. 기본 보기에 대한 간단한 설명은 `aria-roledescription`에 있으며, 해당 기본 보기 구성 요소의 `ROLE_DESCRIPTION` 현지화 심볼에 정의된 값이 있습니다. 키보드 사용자에 대한 탐색 힌트는 `aria-describedby`을 사용하여 제공되며, 사용 힌트의 텍스트는 `USAGE_HINT` 현지화 심볼에서 가져옵니다. 자산에 UserData 필드에 정의된 레이블이 있는 경우 `aria-label` 속성은 해당 레이블 값으로 설정됩니다.

핫 스팟, 지역 및 이미지 맵은 핫 스팟 또는 이미지 맵 레이블의 값을 사용하여 `button` 역할 및 `aria-label` 속성을 사용하는 설명 텍스트 세트를 사용합니다. 사용자가 핫 스팟 또는 이미지 맵에 초점을 맞출 때 키보드 사용자에 대한 탐색 힌트는 `aria-describedby` 를 사용하여 제공되며, 이때 `USAGE_HINT` 로컬라이제이션 심볼에서 오는 사용 힌트에 대한 텍스트가 제공됩니다.
