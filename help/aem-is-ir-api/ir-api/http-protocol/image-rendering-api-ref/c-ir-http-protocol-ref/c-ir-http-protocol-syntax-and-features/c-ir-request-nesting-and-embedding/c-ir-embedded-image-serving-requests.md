---
title: 포함된 이미지 서버 요청
description: 이미지 서버(IS) 요청을 재질 이미지로 사용할 수 있습니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4ece9738-45e0-43c0-ba1c-2a05ef1f39be
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# 포함된 이미지 서버 요청{#embedded-image-server-requests}

이미지 서버(IS) 요청을 재질 이미지로 사용할 수 있습니다.

다음에서 요청을 지정합니다. `src=` 다음과 같은 명령:

` …&src=is( *[!DNL imageServingRequest]*)&…`

다음 `is` 토큰은 대/소문자를 구분합니다.

중첩 요청에는 이미지 제공 루트 경로가 포함되지 않아야 합니다(일반적으로). [!DNL http:// *[!DNL server]*/is/image/"])에 포함되지만 전처리 규칙 토큰을 포함할 수 있습니다.

다음 IS 명령은 중첩 요청( 요청 URL에서 또는 )에 지정될 때 무시됩니다 `catalog::Modifier` 또는 `catalog::PostModifier`):

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

또한 무시됩니다. `attribute::MaxPix` 및 `attribute::DefaultPix` 임베드된 IS 요청에 적용되는 이미지 카탈로그.

중첩된 요청의 결과 이미지에 마스크(알파) 데이터가 포함되어 있으면 항상 자료에 전달됩니다. 단색 배경 이미지 레이어를 사용하여 원하지 않는 알파를 방지합니다.

포함된 IS 요청의 이미지 결과는 다음을 포함하여 선택적으로 캐시될 수 있습니다. `cache=on`. 기본적으로 중간 데이터의 캐싱은 비활성화되어 있습니다. 적절한 기간 내에 중간 이미지를 다른 요청에서 재사용하는 경우에만 캐싱을 활성화해야 합니다. 표준 서버측 캐시 관리가 적용됩니다. 데이터는 무손실 형식으로 캐시됩니다.
