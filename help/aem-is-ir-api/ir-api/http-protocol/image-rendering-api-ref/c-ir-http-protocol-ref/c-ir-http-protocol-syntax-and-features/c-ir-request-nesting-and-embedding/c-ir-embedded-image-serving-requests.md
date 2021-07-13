---
description: 이미지 서버(IS) 요청은 재료 이미지로 사용할 수 있습니다.
solution: Experience Manager
title: 포함된 이미지 서버 요청
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4ece9738-45e0-43c0-ba1c-2a05ef1f39be
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# 포함된 이미지 서버 요청{#embedded-image-server-requests}

이미지 서버(IS) 요청은 재료 이미지로 사용할 수 있습니다.

`src=` 명령에 다음과 같이 요청을 지정합니다.

` …&src=is( *[!DNL imageServingRequest]*)&…`

`is` 토큰은 대/소문자를 구분합니다.

중첩된 요청에는 이미지 제공 루트 경로(일반적으로 [!DNL http:// *[!DNL server]*/is/image/&quot;])가 포함되지 않아야 하지만, 사전 처리 규칙 토큰이 포함될 수 있습니다.

중첩 요청(요청 URL 또는 `catalog::Modifier` 또는 `catalog::PostModifier`에서)에 지정된 경우 다음 IS 명령은 무시됩니다.

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

또한 무시된 IS 요청에 적용되는 이미지 카탈로그의 `attribute::MaxPix` 및 `attribute::DefaultPix`도 무시됩니다.

중첩 요청의 결과 이미지에 마스크(알파) 데이터가 포함되는 경우, 항상 자료에 전달됩니다. 원하지 않는 알파를 방지하려면 단색 배경 이미지 레이어를 사용하십시오.

`cache=on`을 포함하여 포함된 IS 요청의 이미지 결과를 선택적으로 캐시할 수 있습니다. 기본적으로 중간 데이터의 캐싱은 비활성화됩니다. 중간 이미지가 적절한 기간 내에 다른 요청에서 다시 사용되어야 하는 경우에만 캐싱을 활성화해야 합니다. 표준 서버측 캐시 관리가 적용됩니다. 데이터는 무손실 형식으로 캐시됩니다.
