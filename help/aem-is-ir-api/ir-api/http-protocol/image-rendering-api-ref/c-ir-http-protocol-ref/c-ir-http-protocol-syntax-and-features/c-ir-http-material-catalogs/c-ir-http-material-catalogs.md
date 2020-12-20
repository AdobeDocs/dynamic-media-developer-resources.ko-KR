---
description: 자료 카탈로그는 여러 기능을 제공합니다.
seo-description: 자료 카탈로그는 여러 기능을 제공합니다.
seo-title: 자료 카탈로그 *
solution: Experience Manager
title: 자료 카탈로그 *
topic: Scene7 Image Serving - Image Rendering API
uuid: 2a2f371e-0982-47c7-b3da-678a5ff6c7a7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---


# 자료 카탈로그 *{#material-catalogs}

자료 카탈로그는 여러 기능을 제공합니다.

* 모든 재질 속성을 비롯한 재질을 지속적으로 정의할 수 있습니다.

   재료 카탈로그에 정의된 자료는 일련의 재료 속성이 아닌 간단한 ID를 사용하여 참조할 수 있습니다.
* JPEG 품질 또는 기본 응답 이미지 크기와 같은 특정 요청 속성의 기본값을 제공합니다.
* 비네팅, ICC 프로필 및 요청 템플릿을 관리할 수 있습니다.

특정 자료 카탈로그를 정의하지 않아도 기본 카탈로그( [!DNL default.ini])를 통해 자료 카탈로그의 모든 기능을 사용할 수 있습니다.

재료 특성을 사용한 요청에 렌더링 자료를 명시적으로 지정할 수 있지만, 대부분의 경우 재료 카탈로그를 사용하여 웹 사이트에서 자료 세부 사항을 숨기는 것이 더 좋습니다. src= 명령은 명시적 파일 경로 대신 카탈로그 참조를 허용합니다. 카탈로그 항목은 ` [ *[!DNL catId]*/] *[!DNL itemId]*`으로 구성됩니다. 여기서 ` *[!DNL catId]*`은 재료 카탈로그를 식별하고 ` *[!DNL itemId]*`는 카탈로그의 레코드를 식별합니다. ` *[!DNL catId]*`을(를) 지정하지 않으면 세션 카탈로그가 사용됩니다(아래 참조).

(a) ` *[!DNL catId]*`이(가) 재료 카탈로그의 `attribute::RootId` 값과 일치하고 (b) ` *[!DNL recId]*`이 동일한 카탈로그의 catalog::Id 값과 일치하면 카탈로그 레코드가 성공적으로 일치합니다. 성공적인 일치의 경우 자료 속성(`src=` 포함)이 카탈로그 레코드의 데이터로 설정됩니다. MSS에 src= 외에 이 자료에 대한 추가 속성이 포함되어 있으면 카탈로그 레코드의 값을 덮어씁니다.

` *[!DNL recId]*`을(를) 카탈로그 항목과 일치시킬 수 없는 경우 ` *[!DNL catId]*`은(는) 카탈로그에서 `attribute::RootPath`로 대체되고 그 결과 경로는 단순 파일 경로로 간주됩니다. 기타 기본 속성(예:`attribute::Resolution`)도 재료 카탈로그에서 상속될 수 있습니다.

비네팅 및 ICC 프로필은 자료 자체 및 해당 속성과 유사한 자료 카탈로그로 항목화할 수 있습니다. 또한 비네팅 맵은 템플릿의 컨테이너도 제공합니다.

**참조**

재료 카탈로그 참조, [ `src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath`
