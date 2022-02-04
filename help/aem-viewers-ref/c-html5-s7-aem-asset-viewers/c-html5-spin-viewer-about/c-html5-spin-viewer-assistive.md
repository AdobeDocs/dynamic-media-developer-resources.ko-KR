---
title: 보조 기술 지원
description: 모든 뷰어 구성 요소는 화면 판독기와 같은 보조 기술과의 통합을 개선하기 위해 ARIA(Accessible Rich Internet Applications) 역할 및 속성을 지원합니다.
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

모든 뷰어 구성 요소는 화면 판독기와 같은 보조 기술과의 통합을 개선하기 위해 ARIA(Accessible Rich Internet Applications) 역할 및 속성을 지원합니다.

최상위 뷰어 요소에는 역할이 있습니다 `region` 및 `aria-label` 기본적으로 설정된 속성은 뷰어 이름으로 설정됩니다. 를 사용하여 레이블을 제어할 수 있습니다 `Container.LABEL` 로컬라이제이션 기호

버튼에는 역할이 있습니다 `button` 및 설명 텍스트 세트 `aria-label` 속성을 사용합니다. 다음 값 `aria-label` 속성은 단추의 현지화 기호 값에서 채워집니다. 단추가 비활성화되면 `aria-disabled` 속성이 그에 따라 설정됩니다.

기본 보기에는 역할이 있습니다 `application`. 기본 보기에 대한 간단한 설명은 `aria-roledescription`에 정의된 값을 사용하여 `ROLE_DESCRIPTION` 해당 기본 보기 구성 요소의 로컬라이제이션 기호 키보드 사용자에 대한 탐색 힌트는 `aria-describedby`를 설정하는 경우 사용 힌트의 텍스트는 `USAGE_HINT` 로컬라이제이션 기호 자산에 UserData 필드에 정의된 레이블이 있는 경우 `aria-label` 속성이 해당 레이블의 값으로 설정되어 있습니다.
