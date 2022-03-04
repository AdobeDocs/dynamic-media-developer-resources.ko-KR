---
title: 중첩 이미지 렌더링 요청
description: 고급 응용 프로그램의 경우, 이미지 제공(Image Serving)에서 얻은 이미지와 마찬가지로 렌더링 작업 결과를 재료 이미지로 사용할 수 있습니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 52c12786-bbe7-4410-87bb-6245d782a68c
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# 중첩 이미지 렌더링 요청{#nested-image-rendering-requests}

고급 응용 프로그램의 경우, 이미지 제공(Image Serving)에서 얻은 이미지와 마찬가지로 렌더링 작업 결과를 재료 이미지로 사용할 수 있습니다.

렌더링 요청은에서 지정하여 재료 이미지로 사용할 수 있습니다. `src=` 다음과 같이 명령을 수행합니다.

` …&src=ir{ *[!DNL renderRequest]*}&…`

다음 `ir` 토큰은 대/소문자를 구분합니다.

중첩된 요청에는 이미지 렌더링 루트 경로가 포함되지 않아야 합니다(일반적으로 `http:// *[!DNL server]*/ir/render/'`)이지만 사전 처리 규칙 토큰을 포함할 수 있습니다.

중첩 요청(요청 URL 또는 `catalog::Modifier` 또는 `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

또한 무시됩니다 `attribute::MaxPix` 및 `attribute::DefaultPix` 중첩된 렌더링 요청에 적용되는 재료 카탈로그

다음을 포함하여 중첩된 IR 요청의 이미지 결과를 선택적으로 캐시할 수 있습니다 `cache=on`. 기본적으로 중간 데이터의 캐싱은 비활성화됩니다. 중간 이미지가 적절한 기간 내에 다른 요청에서 다시 사용되는 경우에만 캐싱을 활성화해야 합니다. 표준 서버측 캐시 관리가 적용됩니다. 데이터는 무손실 형식으로 캐시됩니다.
