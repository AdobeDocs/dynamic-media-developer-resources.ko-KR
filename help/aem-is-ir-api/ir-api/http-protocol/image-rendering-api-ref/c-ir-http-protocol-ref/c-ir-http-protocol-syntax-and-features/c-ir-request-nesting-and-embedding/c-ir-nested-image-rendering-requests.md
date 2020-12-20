---
description: 고급 응용 프로그램의 경우 이미지 제공에서 얻은 이미지와 마찬가지로 렌더링 작업의 결과를 재료 이미지로 사용할 수 있습니다.
seo-description: 고급 응용 프로그램의 경우 이미지 제공에서 얻은 이미지와 마찬가지로 렌더링 작업의 결과를 재료 이미지로 사용할 수 있습니다.
seo-title: 중첩된 이미지 렌더링 요청
solution: Experience Manager
title: 중첩된 이미지 렌더링 요청
topic: Scene7 Image Serving - Image Rendering API
uuid: 12551bd5-ff5f-45d6-81e9-5ba0be47a425
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---


# 중첩 이미지 렌더링 요청{#nested-image-rendering-requests}

고급 응용 프로그램의 경우 이미지 제공에서 얻은 이미지와 마찬가지로 렌더링 작업의 결과를 재료 이미지로 사용할 수 있습니다.

렌더링 요청은 다음과 같이 `src=` 명령에 지정하여 재료 이미지로 사용할 수 있습니다.

` …&src=ir{ *[!DNL renderRequest]*}&…`

`ir` 토큰은 대/소문자를 구분합니다.

중첩된 요청에는 이미지 렌더링 루트 경로(일반적으로 `http:// *[!DNL server]*/ir/render/'`)가 포함되지 않아야 하지만 사전 처리 규칙 토큰이 포함될 수 있습니다.

중첩 요청에 지정된 경우(요청 URL 또는 `catalog::Modifier` 또는 `catalog::PostModifier`) 다음 명령이 무시됩니다.

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

또한 무시되는 것은 중첩된 렌더링 요청에 적용되는 재료 카탈로그의 `attribute::MaxPix` 및 `attribute::DefaultPix`입니다.

중첩된 IR 요청의 이미지 결과는 선택적으로 `cache=on`을 포함하여 캐시할 수 있습니다. 기본적으로 중간 데이터의 캐싱은 비활성화됩니다. 캐시는 중간 이미지가 적절한 기간 내에 다른 요청에서 다시 사용되어야 하는 경우에만 활성화되어야 합니다. 표준 서버측 캐시 관리가 적용됩니다. 데이터는 손실 없는 형식으로 캐시됩니다.
