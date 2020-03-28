---
description: 모든 뷰어 구성 요소는 화면 판독기와 같은 보조 기술과의 통합을 개선하기 위해 ARIA(액세스 가능한 리치 인터넷 애플리케이션) 역할 및 속성을 지원합니다.
seo-description: 모든 뷰어 구성 요소는 화면 판독기와 같은 보조 기술과의 통합을 개선하기 위해 ARIA(액세스 가능한 리치 인터넷 애플리케이션) 역할 및 속성을 지원합니다.
seo-title: 보조 기술 지원
solution: Experience Manager
title: 보조 기술 지원
topic: Dynamic media
uuid: 5f6a021f-750c-40e1-be01-86c3750fd25f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 보조 기술 지원{#assistive-technology-support}

모든 뷰어 구성 요소는 화면 판독기와 같은 보조 기술과의 통합을 개선하기 위해 ARIA(액세스 가능한 리치 인터넷 애플리케이션) 역할 및 속성을 지원합니다.

최상위 뷰어 요소에는 기본적으로 뷰어 이름으로 설정된 역할 `region` 및 `aria-label` 속성이 있습니다. 현지화 기호로 레이블을 제어할 수 `Container.LABEL` 있습니다.

기본 보기에는 역할이 `application`있습니다. 기본 보기에 대한 간단한 설명은 에서 `aria-roledescription`제공되며 해당 기본 보기 구성 요소의 `ROLE_DESCRIPTION` 현지화 기호로 정의된 값입니다. 키보드 사용자에 대한 탐색 힌트는 를 사용하여 `aria-describedby`제공되며, 사용 힌트에 대한 텍스트는 `USAGE_HINT` 현지화 기호에서 가져옵니다. 자산에 UserData 필드에 정의된 레이블이 있는 경우, `aria-label` 속성은 해당 레이블의 값으로 설정됩니다.

핫 스팟, 지역 및 이미지 맵은 핫 스팟 또는 이미지 맵 레이블 값과 함께 역할 `button` 및 설명 텍스트 `aria-label` 세트가 있습니다. 사용자가 핫 스팟 또는 이미지 맵에 초점을 맞출 때 키보드 사용자에 대한 탐색 힌트가 `aria-describedby``USAGE_HINT` 제공되고 현지화 기호에서 나오는 사용 힌트에 대한 텍스트가 표시됩니다.
