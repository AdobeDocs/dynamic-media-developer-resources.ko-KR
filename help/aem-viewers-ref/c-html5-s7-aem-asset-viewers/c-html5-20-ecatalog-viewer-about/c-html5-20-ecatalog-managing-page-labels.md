---
title: 페이지 레이블 관리
description: 페이지 레이블 관리
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: b62b5cb8-6100-4d0f-afd8-e6daa6ce6539
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# 페이지 레이블 관리{#managing-page-labels}

뷰어 사용자 인터페이스에는 페이지 레이블이 표시되는 두 가지 위치, 즉 썸네일 모드와 목차 드롭다운이 있습니다.

정의할 수 있는 세 가지 유형의 레이블은 다음과 같습니다.

* 기호 현지화 메커니즘을 사용하여 작성자가 정의한 레이블입니다.
* Dynamic Media Classic 내부의 백엔드에서 작성자가 정의한 레이블.
* 뷰어에서 자동으로 생성된 레이블입니다.

기호 기반 레이블은 [사용자 인터페이스 요소의 지역화](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)에 설명된 대로 `MediaSet.LABEL_XX[_YY]` 및 `MediaSet.LABEL_DELIM` 기호를 사용하여 정의됩니다. 전체 전자 카탈로그 스프레드에 대해 이러한 레이블을 정의할 수 있습니다. 이 경우 짧은 SYMBOL 구문(`MediaSet.LABEL_XX`)을 사용해야 합니다. 또는 전체 SYMBOL 구문(`MediaSet.LABEL_XX_YY`)을 사용하여 각 페이지에 대해 개별적으로 지정하십시오.

전자 카탈로그 스프레드의 두 페이지에 대한 레이블을 정의하면 뷰어는 `MediaSet.LABEL_DELIM` SYMBOL을 사용하여 이러한 레이블을 하나의 문자열로 연결합니다. SYMBOL 기반 레이블은 백엔드에 정의된 레이블이나 뷰어에서 자동으로 생성한 레이블보다 우선합니다.

Dynamic Media Classic에 정의된 레이블은 개별 페이지 이미지의 UserData 레코드에 저장됩니다. SYMBOL 기반 레이블과 동일합니다. 즉, 전자 카탈로그 스프레드의 두 페이지에 정의된 레이블이 있는 경우, 가로 모드에서 `MediaSet.LABEL_DELIM` SYMBOL을 사용하여 연결됩니다. Dynamic Media Classic 레이블은 자동으로 생성된 레이블보다 우선하지만 SYMBOL 기반 레이블에 의해 재정의됩니다.

자동으로 생성된 레이블은 전자 카탈로그의 모든 페이지에 지정된 순차적 번호입니다. 기호 기반 레이블이 정의되어 있거나 Dynamic Media Classic 레이블이 정의된 경우 자동으로 생성된 레이블은 지정된 스프레드에 대해 무시됩니다.

목차에서는 `showdefault` 매개 변수를 사용하여 자동으로 생성된 레이블을 표시하지 않도록 설정할 수 있습니다.
