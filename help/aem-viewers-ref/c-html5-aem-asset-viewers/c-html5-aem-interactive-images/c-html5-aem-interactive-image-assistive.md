---
title: 보조 기술 지원
description: 모든 뷰어 구성 요소는 ARIA(Accessible Rich Internet Applications) 역할 및 속성을 지원하여 화면 판독기와 같은 보조 기술과의 통합을 향상시킵니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images,Accessibility
role: Developer,User
exl-id: 39e64f35-543f-4977-a97a-0daa93786ff3
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# 보조 기술 지원{#assistive-technology-support}

모든 뷰어 구성 요소는 ARIA(Accessible Rich Internet Applications) 역할 및 속성을 지원하여 화면 판독기와 같은 보조 기술과의 통합을 향상시킵니다.

최상위 뷰어 요소에 역할이 있음 `region` 및 `aria-label` 속성이 기본적으로 뷰어의 이름으로 설정됩니다. 다음을 사용하여 레이블을 제어할 수 있습니다. `Container.LABEL` 지역화 기호.

기본 보기에 역할이 있습니다. `application`. 기본 보기에 대한 간략한 설명은에 제공됩니다. `aria-roledescription`로 정의된 값 사용 `ROLE_DESCRIPTION` 해당 기본 보기 구성 요소의 현지화 기호. 키보드 사용자를 위한 탐색 힌트는 `aria-describedby`, 사용 힌트의 텍스트는 `USAGE_HINT` 지역화 기호. 에셋에 UserData 필드에 정의된 레이블이 있는 경우 `aria-label` 속성은 이러한 레이블의 값으로 설정됩니다.

핫스팟, 영역 및 이미지 맵에는 역할이 있습니다 `button` 및 설명 텍스트 세트 `aria-label` 속성(핫스팟 또는 이미지 맵 레이블 값 포함) 사용자가 핫스팟 또는 이미지 맵에 초점을 맞추면 다음을 사용하여 키보드 사용자를 위한 탐색 힌트가 제공됩니다 `aria-describedby`에서 나오는 사용 힌트에 대한 텍스트가 있는 `USAGE_HINT` 지역화 기호.
