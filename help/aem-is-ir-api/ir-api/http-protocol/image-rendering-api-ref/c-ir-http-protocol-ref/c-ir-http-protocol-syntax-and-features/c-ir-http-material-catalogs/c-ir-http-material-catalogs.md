---
title: 자료 카탈로그
description: 자료 카탈로그는 몇 가지 기능을 제공합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 502f80f5-fdd1-468b-89a9-64cc9128d655
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# 자료 카탈로그 {#material-catalogs}

자료 카탈로그는 몇 가지 기능을 제공합니다.

* 모든 재료 특성을 포함하여 재료를 지속적으로 정의할 수 있습니다.

  재료 카탈로그에 정의된 재료는 재료 특성 세트가 아니라 간단한 ID를 사용하여 참조할 수 있습니다.
* JPEG 품질 또는 기본 응답 이미지 크기와 같은 특정 요청 속성에 대한 기본값을 제공합니다.
* 비네팅, ICC 프로파일 및 요청 템플릿을 관리합니다.

특정 재질 카탈로그가 정의되지 않은 경우에도 기본 카탈로그([!DNL default.ini])를 통해 재질 카탈로그의 모든 기능을 사용할 수 있습니다.

렌더링 자료는 재질 특성을 사용하여 요청에 명시적으로 지정할 수 있지만 재질 카탈로그를 사용하여 웹 사이트에서 자료의 세부 정보를 숨기는 것이 더 바람직한 경우가 많습니다. src= 명령은 명시적 파일 경로 대신 카탈로그 참조를 허용합니다. 카탈로그 항목은 ` [ *[!DNL catId]*/] *[!DNL itemId]*`(으)로 구성됩니다. 여기서 ` *[!DNL catId]*`은(는) 재질 카탈로그를 식별하며 ` *[!DNL itemId]*`은(는) 카탈로그에서 레코드를 식별합니다. ` *[!DNL catId]*`을(를) 지정하지 않으면 세션 카탈로그가 사용됩니다(아래 참조).

(a) ` *[!DNL catId]*`이(가) 재질 카탈로그의 `attribute::RootId` 값과 일치하고 (b) ` *[!DNL recId]*`이(가) 동일한 카탈로그의 카탈로그::Id 값과 일치하는 경우 카탈로그 레코드가 정상적으로 일치합니다. 일치하는 항목이 있으면 재질(`src=` 포함)의 특성이 카탈로그 레코드의 데이터로 설정됩니다. MSS에 src= 외에 이 자료에 대한 추가 속성이 포함된 경우 카탈로그 레코드의 값을 재정의합니다.

` *[!DNL recId]*`을(를) 카탈로그 항목과 일치시킬 수 없는 경우 ` *[!DNL catId]*`이(가) 카탈로그의 `attribute::RootPath`(으)로 바뀌고 결과 경로는 단순 파일 경로로 간주됩니다. 다른 기본 특성(예: `attribute::Resolution`)도 재질 카탈로그에서 상속될 수 있습니다.

비네팅 및 ICC 프로파일은 재료 자체와 유사한 재료 카탈로그에 항목별로 나열할 수 있으며, 지정된 특성도 있습니다. 또한 비네팅 맵은 템플릿을 위한 컨테이너도 제공합니다.

**참고 항목**

재질 카탈로그 참조, [`src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath`
