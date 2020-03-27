---
description: 널
seo-description: 널
seo-title: 페이지 레이블 관리
solution: Experience Manager
title: 페이지 레이블 관리
topic: Dynamic media
uuid: 49444fe6-ef34-4e5b-a293-e23830a67b4d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 페이지 레이블 관리{#managing-page-labels}

뷰어 사용자 인터페이스에는 페이지 레이블이 표시되는 두 가지 위치가 있습니다.축소판 모드 및 목차 드롭다운

다음과 같은 세 가지 유형의 레이블을 정의할 수 있습니다.

* SYMBOL 현지화 메커니즘을 사용하여 작성자가 정의한 레이블입니다.
* 백엔드, Scene7 Publishing System 내에서 작성자가 정의한 레이블입니다.
* 뷰어에서 자동으로 생성된 레이블.

SYMBOL 기반 레이블은 사용자 인터페이스 요소의 현지화에 설명된 대로 `MediaSet.LABEL_XX[_YY]` 및 `MediaSet.LABEL_DELIM` SYMBOL을 [사용하여 정의됩니다](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74). 전체 ecatalog 스프레드에 대해 이러한 레이블을 정의할 수 있습니다. 이 경우 짧은 SYMBOL 구문( `MediaSet.LABEL_XX`)을 사용해야 합니다. 또는 전체 기호 구문( `MediaSet.LABEL_XX_YY`)을 사용하여 각 페이지에 대해 개별적으로 지정합니다.

카탈로그 스프레드에서 두 페이지에 대한 레이블을 정의할 때 뷰어는 SYMBOL을 사용하여 이러한 레이블을 하나의 문자열로 `MediaSet.LABEL_DELIM` 연결합니다. 심볼 기반 레이블은 뷰어에서 자동으로 생성된 레이블이나 백엔드에 정의된 레이블보다 우선합니다.

Scene7 Publishing System에 정의된 레이블은 개별 페이지 이미지의 사용자 데이터 레코드에 저장됩니다. 심볼 기반 레이블과 동일합니다. 즉, 카탈로그 스프레드의 두 페이지 모두에 레이블이 정의된 경우 가로 모드의 SYMBOL을 사용하여 `MediaSet.LABEL_DELIM` 연결됩니다. Scene7 Publishing System 레이블은 자동으로 생성된 레이블보다 우선하지만 SYMBOL 기반 레이블로 재정의됩니다.

자동으로 생성된 레이블은 카탈로그의 모든 페이지에 할당된 순차적 번호입니다. 지정된 스프레드에 SYMBOL 기반 레이블이 정의되거나 Scene7 Publishing System 레이블이 정의된 경우 자동으로 생성된 레이블이 무시됩니다.

목차에서는 `showdefault` 매개 변수를 사용하여 자동으로 생성된 레이블의 표시를 비활성화할 수 있습니다.
