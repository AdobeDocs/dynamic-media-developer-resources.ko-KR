---
description: 템플릿은 여러 이미지 레이어를 합성하거나 rtf 형식의 텍스트를 포함하는 요청의 길이와 복잡성을 줄이는 데 사용할 수 있습니다.
seo-description: 템플릿은 여러 이미지 레이어를 합성하거나 rtf 형식의 텍스트를 포함하는 요청의 길이와 복잡성을 줄이는 데 사용할 수 있습니다.
seo-title: 템플릿
solution: Experience Manager
title: 템플릿
topic: Scene7 Image Serving - Image Rendering API
uuid: 54830d1f-40ad-4bf2-8e3d-d3e4d4ab57b9
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# 템플릿{#templates}

템플릿은 여러 이미지 레이어를 합성하거나 rtf 형식의 텍스트를 포함하는 요청의 길이와 복잡성을 줄이는 데 사용할 수 있습니다.

사용자 지정 변수를 사용하여 템플릿 사용을 더욱 간소화할 수 있습니다. 템플릿은 종종 이미지 또는 텍스트를 손쉽게 교환하거나 런타임 시 다른 옵션을 설정할 수 있도록 설정됩니다.

템플릿은 이미지 카탈로그에 레코드로 저장되며, 템플릿 본문은 `catalog::Modifier` 필드에 있고, `catalog::Path` 필드는 비어 있거나 동적으로 변경할 수 없는 정적 배경 이미지를 지정합니다.

템플릿은 요청 URL의 경로 구성 요소나 `template=` 명령으로 지정됩니다. 대부분의 응용 프로그램에서는 이 `template=` 명령을 사용하여 템플릿을 지정하는 것이 좋습니다. 이 `template=`명령은 `catalog::PostModifier` 필드에서 발생해서는 안 되며 중첩된 IS 요청의 `catalog::Modifier` 필드에서만 발생할 수 `src=is{...}` 있습니다. 템플릿 레코드는 `src=` 또는 `mask=`명령에서 참조할 수 없습니다.

템플릿에 포함된 모든 `src=` 또는 `mask=`명령은 요청의 기본 카탈로그 또는 다른 이미지 카탈로그로 확인할 수 있습니다. 명시적으로 지정하지 `rootId` 않으면 기본 카탈로그가 가정됩니다. 로 지정된 템플릿은 기본 카탈로그 또는 다른 이미지 카탈로그에도 `template=` 있을 수 있습니다.

템플릿에 사용된 모든 변수에 대한 기본 정의를 항상 포함하는 것이 좋습니다. 이렇게 하면 템플릿에서 어떤 변수가 사용되고 있는지 알 필요 없이 템플릿의 이미지 출력을 `attribute::RootId` 및 `catalog::Id`를 지정하여 간단히 볼 수 있습니다.

사전 정의된 경로 대체 변수를 `$object$` 사용하여 URL 경로에 지정된 이미지 개체를 중첩된 요청이나 포함된 요청에서도 레이어 소스 또는 마스크( `src=` 또는 `mask=`)에 적용할 수 있습니다.

* [예 A](r-example-a.md)
* [예 B](r-example-b.md)
* [예 C](r-example-c.md)
