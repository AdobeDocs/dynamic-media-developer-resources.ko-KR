---
description: 이미지 서버(IS 파섹) 요청을 재료 이미지로 사용할 수 있습니다.
seo-description: 이미지 서버(IS 파섹) 요청을 재료 이미지로 사용할 수 있습니다.
seo-title: 포함된 이미지 서버 요청
solution: Experience Manager
title: 포함된 이미지 서버 요청
topic: Scene7 Image Serving - Image Rendering API
uuid: dd72880d-8824-40b3-a5da-0f6ff4922939
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 포함된 이미지 서버 요청{#embedded-image-server-requests}

이미지 서버(IS 파섹) 요청을 재료 이미지로 사용할 수 있습니다.

명령에서 다음과 같이 요청을 `src=` 지정합니다.

` …&src=is( *[!DNL imageServingRequest]*)&…`

토큰은 대소문자를 구분합니다. `is`

중첩 요청에는 이미지 제공 루트 경로(일반적으로 [!DNL http:// *[!DNL server]*/is/image/&quot;])가 포함되어서는 안 되며, 사전 처리 규칙 토큰이 포함될 수 있습니다.

다음 IS 명령은 중첩된 요청에 지정되면 무시됩니다(요청 URL 또는 `catalog::Modifier` 또는 `catalog::PostModifier`에서).

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

또한 무시된 이미지 카탈로그는 포함된 IS 요청에 적용되는 `attribute::MaxPix` 및 `attribute::DefaultPix` 이미지 카탈로그입니다.

중첩된 요청의 결과 이미지에 마스크(알파) 데이터가 포함되어 있으면 항상 자료에 전달됩니다. 단색 배경 이미지 레이어를 사용하여 원하지 않는 알파를 방지할 수 있습니다.

포함된 IS 요청의 이미지 결과는 포함시킴으로써 선택적으로 캐시될 수 `cache=on`있습니다. 기본적으로 중간 데이터의 캐싱은 비활성화됩니다. 중간 이미지를 적절한 기간 내에 다른 요청에서 다시 사용할 것으로 예상되는 경우에만 캐싱을 활성화해야 합니다. 표준 서버측 캐시 관리가 적용됩니다. 데이터는 손실 없는 형식으로 캐시됩니다.
