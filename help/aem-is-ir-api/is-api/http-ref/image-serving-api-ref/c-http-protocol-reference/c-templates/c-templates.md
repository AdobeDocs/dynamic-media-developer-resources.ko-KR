---
title: 템플릿
description: 템플릿은 여러 이미지 레이어를 합성하거나 rtf 형식의 텍스트를 포함하는 요청의 길이 및 복잡성을 줄이는 데 사용할 수 있습니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef49cf8a-4621-4114-aae5-5178f6a5160d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# 템플릿{#templates}

템플릿은 여러 이미지 레이어를 합성하거나 rtf 형식의 텍스트를 포함하는 요청의 길이 및 복잡성을 줄이는 데 사용할 수 있습니다.

사용자 지정 변수를 사용하여 템플릿 사용을 더 단순화할 수 있습니다. 템플릿은 종종 런타임 시 이미지 또는 텍스트를 쉽게 교체하거나 다른 옵션을 설정할 수 있도록 설정됩니다.

템플릿은 이미지 카탈로그에 레코드로 저장됩니다. 템플릿 본문은 `catalog::Modifier` 필드에 있고 `catalog::Path` 필드는 비어 있거나 동적으로 변경할 수 없는 정적 배경 이미지를 지정합니다.

`template=` 명령 또는 요청 URL의 경로 구성 요소에서 템플릿을 지정합니다. 대부분의 응용 프로그램에서는 `template=` 명령을 사용하여 템플릿을 지정하는 것이 좋습니다. `template=` 명령은 `catalog::PostModifier` 필드에서 발생하지 않아야 하며 중첩된 IS 요청의 `catalog::Modifier` 필드(즉, `src=is{...}` 구문)에서만 발생할 수 있습니다. 템플릿 레코드가 `src=` 또는 `mask=` 명령에 참조되지 않을 수 있습니다.

템플릿에 포함된 `src=` 또는 `mask=` 명령은 요청의 기본 카탈로그나 다른 이미지 카탈로그로 확인될 수 있습니다. `rootId`을(를) 명시적으로 지정하지 않으면 기본 카탈로그로 간주됩니다. `template=`(으)로 지정된 템플릿은 주 카탈로그 또는 다른 이미지 카탈로그에도 있을 수 있습니다.

템플릿에 사용된 모든 변수에 대한 기본 정의를 항상 포함하는 것이 좋습니다. 이렇게 하면 템플릿에 사용되는 변수를 알 필요 없이 해당 `attribute::RootId` 및 `catalog::Id`을(를) 지정하여 템플릿의 이미지 출력을 항상 볼 수 있습니다.

미리 정의된 경로 대체 변수 `$object$`을(를) 사용하여 중첩된 요청이나 포함된 요청에서도 URL 경로에 지정된 이미지 개체를 모든 레이어 소스나 마스크(`src=` 또는 `mask=`)에 적용할 수 있습니다.

* [예 A](r-example-a.md)
* [예 B](r-example-b.md)
* [예 C](r-example-c.md)
