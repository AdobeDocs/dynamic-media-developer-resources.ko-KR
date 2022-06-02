---
title: 템플릿
description: 템플릿은 여러 이미지 레이어를 합성하거나 rtf 형식의 텍스트를 포함하는 요청의 길이와 복잡성을 줄이는 데 사용할 수 있습니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef49cf8a-4621-4114-aae5-5178f6a5160d
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# 템플릿{#templates}

템플릿은 여러 이미지 레이어를 합성하거나 rtf 형식의 텍스트를 포함하는 요청의 길이와 복잡성을 줄이는 데 사용할 수 있습니다.

사용자 지정 변수를 사용하여 템플릿 사용을 더 단순화할 수 있습니다. 템플릿은 종종 이미지 또는 텍스트를 쉽게 교체하거나 런타임 시 다른 옵션을 설정할 수 있도록 설정됩니다.

템플릿은 이미지 카탈로그에 레코드로 저장되며 템플릿 본문은 `catalog::Modifier` 필드 및 `catalog::Path` 필드가 비어 있거나 동적으로 변경할 수 없는 정적 배경 이미지를 지정합니다.

템플릿은 `template=` 명령 또는 요청 URL의 경로 구성 요소에 있는 를 나타냅니다. 대부분의 애플리케이션의 경우 `template=` 템플릿을 지정하는 명령 다음 `template=`명령은 `catalog::PostModifier` 필드 및 는 `catalog::Modifier` 중첩 IS 요청의 필드(즉, `src=is{...}` 구성)를 사용하여 규칙 세트를 만듭니다. 템플릿 레코드는 다음에서 참조되지 않을 수 있습니다. `src=` 또는 `mask=`명령.

임의 `src=` 또는 `mask=`템플릿에 포함된 명령은 요청의 기본 카탈로그나 다른 이미지 카탈로그로 확인할 수 있습니다. 없는 경우 `rootId` 이 명시적으로 지정되어 있으면 주 카탈로그가 가정합니다. 에 지정된 템플릿 `template=` 주 카탈로그 또는 다른 이미지 카탈로그에 있을 수도 있습니다.

템플릿에 사용된 모든 변수에 대한 기본 정의를 항상 포함하는 것이 좋습니다. 이렇게 하면 템플릿의 이미지 출력을 단순히 지정하여 항상 볼 수 있습니다 `attribute::RootId` 및 `catalog::Id`: 템플릿에 어떤 변수가 사용되는지 알 필요가 없습니다.

사전 정의된 경로 대체 변수 `$object$` url 경로에 지정된 이미지 개체를 레이어 소스 또는 마스크에 적용하는 데 사용할 수 있습니다( `src=` 또는 `mask=`), 중첩된 요청이나 포함된 요청에서도 사용할 수 있습니다.

* [예 A](r-example-a.md)
* [예 B](r-example-b.md)
* [예 C](r-example-c.md)
