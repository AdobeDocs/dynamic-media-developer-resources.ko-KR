---
title: 보조 기술 지원
description: 모든 뷰어 구성 요소는 ARIA(Accessible Rich Internet Applications) 역할 및 속성을 지원하여 화면 판독기와 같은 보조 기술과의 통합을 향상시킵니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom,Accessibility
role: Developer,User
exl-id: f2f36520-f6dd-4baa-abf0-48a846882acb
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# 보조 기술 지원{#assistive-technology-support}

모든 뷰어 구성 요소는 ARIA(Accessible Rich Internet Applications) 역할 및 속성을 지원하여 화면 판독기와 같은 보조 기술과의 통합을 향상시킵니다.

최상위 뷰어 요소에는 기본적으로 뷰어 이름으로 설정된 `region` 역할 및 `aria-label` 특성이 있습니다. `Container.LABEL` 지역화 기호를 사용하여 레이블을 제어할 수 있습니다.

단추에는 `aria-label` 특성이 있는 설명 텍스트와 `button` 역할이 설정되어 있습니다. `aria-label` 특성 값은 단추의 현지화 기호 값에서 채워집니다. 단추를 사용하지 않도록 설정하면 `aria-disabled` 특성이 그에 따라 설정됩니다.

기본 보기에 `application` 역할이 있습니다. 기본 보기에 대한 간략한 설명이 `aria-roledescription`에 제공됩니다. 이 값은 해당 기본 보기 구성 요소의 `ROLE_DESCRIPTION` 지역화 기호로 정의됩니다. `aria-describedby`을(를) 사용하여 키보드 사용자를 위한 탐색 힌트가 제공됩니다. 사용 힌트에 대한 텍스트는 `USAGE_HINT` 지역화 기호에서 가져옵니다. 에셋에 UserData 필드에 정의된 레이블이 있는 경우 `aria-label` 특성은 해당 레이블의 값으로 설정됩니다.
