---
title: 보조 기술 지원
description: 모든 뷰어 구성 요소는 ARIA(Accessible Rich Internet Applications) 역할 및 속성을 지원하여 화면 판독기와 같은 보조 기술과의 통합을 향상시킵니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets,Accessibility
role: Developer,User
exl-id: f0cde820-237c-4594-8a16-d272af4c976b
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 0%

---

# 보조 기술 지원{#assistive-technology-support}

모든 뷰어 구성 요소는 ARIA(Accessible Rich Internet Applications) 역할 및 속성을 지원하여 화면 판독기와 같은 보조 기술과의 통합을 향상시킵니다.

최상위 뷰어 요소에 역할이 있음 `region` 및 `aria-label` 속성이 기본적으로 뷰어의 이름으로 설정됩니다. 다음을 사용하여 레이블을 제어할 수 있습니다. `Container.LABEL` 지역화 기호.

단추에 역할 있음 `button` 및 설명 텍스트 세트 `aria-label` 특성. 값: `aria-label` 속성은 버튼의 현지화 기호 값에서 채워집니다. 버튼이 비활성화되면 `aria-disabled` 속성이 적절하게 설정됩니다.

기본 보기에 역할이 있습니다. `application`. 기본 보기에 대한 간략한 설명은에 제공됩니다. `aria-roledescription`로 정의된 값 사용 `ROLE_DESCRIPTION` 해당 기본 보기 구성 요소의 현지화 기호. 키보드 사용자를 위한 탐색 힌트는 `aria-describedby`, 사용 힌트의 텍스트는 `USAGE_HINT` 지역화 기호. 에셋에 UserData 필드에 정의된 레이블이 있는 경우 `aria-label` 속성은 이러한 레이블의 값으로 설정됩니다.
