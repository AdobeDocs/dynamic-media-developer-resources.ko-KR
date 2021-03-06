---
description: 페이지 레이블 관리
solution: Experience Manager
title: 페이지 레이블 관리
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog 검색
role: Developer,User
exl-id: 73c3904f-678f-47c4-b895-86671402df79
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# 페이지 레이블 관리{#managing-page-labels}

뷰어 사용자 인터페이스에는 페이지 레이블이 표시되는 두 개의 위치가 있습니다. 축소판 모드 및 목차 드롭다운

정의할 수 있는 레이블에는 다음 세 가지 유형이 있습니다.

* SYMBOL 현지화 메커니즘을 사용하여 작성자가 정의한 레이블입니다.
* Dynamic Media Classic 내에서 백엔드의 작성자가 정의한 레이블입니다.
* 뷰어에서 자동으로 생성된 레이블입니다.

기호 기반 레이블은 [사용자 인터페이스 요소 현지화](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)에 설명된 대로 `MediaSet.LABEL_XX[_YY]` 및 `MediaSet.LABEL_DELIM` 기호를 사용하여 정의됩니다. 전체 전자 카탈로그 스프레드에 대해 이러한 레이블을 정의할 수 있습니다. 이 경우 짧은 기호 구문( `MediaSet.LABEL_XX`)을 사용해야 합니다. 또는 전체 기호 구문( `MediaSet.LABEL_XX_YY`)을 사용하여 각 페이지에 대해 개별적으로 지정합니다.

전자 카탈로그 스프레드의 두 페이지에 대한 레이블을 정의할 때 뷰어는 `MediaSet.LABEL_DELIM` SYMBOL을 사용하여 이러한 레이블을 하나의 문자열로 연결합니다. 기호 기반 레이블은 백엔드에 정의되어 있거나 뷰어가 자동으로 생성한 레이블보다 우선합니다.

Dynamic Media Classic에 정의된 레이블은 개별 페이지 이미지의 UserData 레코드에 저장됩니다. 기호 기반 레이블과 동일합니다. 즉, 전자 카탈로그 스프레드의 두 페이지에 레이블이 정의된 경우 가로 모드에서 `MediaSet.LABEL_DELIM` SYMBOL을 사용하여 연결합니다. Dynamic Media Classic 레이블은 자동으로 생성된 레이블보다 우선하지만 SYMBOL 기반 레이블로 재정의됩니다.

자동 생성된 레이블은 전자 카탈로그의 모든 페이지에 할당된 순차적 번호입니다. 정의된 기호 기반 레이블이나 Dynamic Media Classic 레이블이 정의된 경우 지정된 스프레드에 대해 자동 생성된 레이블은 무시됩니다.

목차에서는 `showdefault` 매개 변수를 사용하여 자동으로 생성된 레이블의 표시를 비활성화할 수 있습니다.
