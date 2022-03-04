---
title: 재료 카탈로그
description: 자재 카탈로그는 여러 기능을 제공합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 502f80f5-fdd1-468b-89a9-64cc9128d655
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# 재료 카탈로그 {#material-catalogs}

자재 카탈로그는 여러 기능을 제공합니다.

* 모든 재료 특성을 포함한 재료의 지속적인 정의를 허용합니다.

   재료 카탈로그에 정의된 자료는 재료 특성 세트가 아닌 간단한 ID를 사용하여 참조할 수 있습니다.
* JPEG 품질 또는 기본 회신 이미지 크기와 같은 특정 요청 속성에 대한 기본값을 제공합니다.
* 비네팅, ICC 프로필 및 요청 템플릿을 관리합니다.

특정 자재 카탈로그가 정의되지 않은 경우에도 기본 카탈로그( [!DNL default.ini]).

재료 속성을 사용하는 요청에 렌더링 재료를 명시적으로 지정할 수 있지만, 재료 카탈로그를 사용하여 웹 사이트에서 재료의 세부 사항을 숨기는 것이 더 좋습니다. src= 명령은 명시적 파일 경로 대신 카탈로그 참조를 허용합니다. 카탈로그 항목은 ` [ *[!DNL catId]*/] *[!DNL itemId]*`, 위치 ` *[!DNL catId]*` 재료 카탈로그를 식별하고 ` *[!DNL itemId]*` 카탈로그에서 레코드를 식별합니다. If ` *[!DNL catId]*` 를 지정하지 않으면 세션 카탈로그가 사용됩니다(아래 참조).

카탈로그 레코드가 일치하는 경우 (a) ` *[!DNL catId]*` 일치 `attribute::RootId` 재료 카탈로그 값 및 (b) ` *[!DNL recId]*` 동일한 카탈로그의 catalog::Id 값과 일치합니다. 일치하는 항목이 있으면 재료 속성(포함) `src=`)가 카탈로그 레코드의 데이터로 설정됩니다. MSS에 src= 이외의 이 자료에 대한 추가 특성이 포함되어 있으면 카탈로그 레코드의 값을 덮어씁니다.

If ` *[!DNL recId]*` 카탈로그 항목과 일치할 수 없습니다. ` *[!DNL catId]*` 이 `attribute::RootPath` 그런 다음 카탈로그에서 결과 경로를 단순 파일 경로로 가정합니다. 기타 기본 속성(예: `attribute::Resolution`)은 재료 카탈로그에서 상속될 수도 있습니다.

비네팅 및 ICC 프로파일은 자료 자체와 유사한 자료 카탈로그 및 해당 등록 정보로 항목화할 수 있습니다. 또한 비네팅 맵은 템플릿용 컨테이너도 제공합니다.

**참조**

자재 카탈로그 참조, [ `src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath`
