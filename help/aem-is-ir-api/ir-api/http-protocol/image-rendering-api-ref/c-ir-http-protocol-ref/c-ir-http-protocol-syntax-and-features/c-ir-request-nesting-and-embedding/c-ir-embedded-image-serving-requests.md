---
title: 포함된 이미지 서버 요청
description: 이미지 서버(IS) 요청을 재질 이미지로 사용할 수 있습니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4ece9738-45e0-43c0-ba1c-2a05ef1f39be
TQID: 'https://experienceleague.adobe.com/dt-baBh9jAyJdjqopFR3AoqRvz5zqLzi8B3SnE04xEs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 183
ht-degree: 0%

---

# 포함된 이미지 서버 요청{#embedded-image-server-requests}

이미지 서버(IS) 요청을 재질 이미지로 사용할 수 있습니다.

`src=` 명령에 요청을 다음과 같이 지정합니다.

` …&src=is( *[!DNL imageServingRequest]*)&…`

`is` 토큰은 대/소문자를 구분합니다.

중첩 요청에는 이미지 제공 루트 경로(일반적으로  [!DNL http:// *[!DNL server]*/is/image/"])가 포함되지 않아야 하지만 전처리 규칙 토큰이 포함될 수 있습니다.

중첩 요청(요청 URL이나 `catalog::Modifier` 또는 `catalog::PostModifier`에서)에 지정할 때 다음 IS 명령이 무시됩니다.

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

포함된 IS 요청에 적용되는 이미지 카탈로그의 `attribute::MaxPix` 및 `attribute::DefaultPix`도 무시됩니다.

중첩된 요청의 결과 이미지에 마스크(알파) 데이터가 포함되어 있으면 항상 자료에 전달됩니다. 단색 배경 이미지 레이어를 사용하여 원하지 않는 알파를 방지합니다.

포함된 IS 요청의 이미지 결과는 `cache=on`을(를) 포함하여 선택적으로 캐시할 수 있습니다. 기본적으로 중간 데이터의 캐싱은 비활성화되어 있습니다. 적절한 기간 내에 중간 이미지를 다른 요청에서 재사용하는 경우에만 캐싱을 활성화해야 합니다. 표준 서버측 캐시 관리가 적용됩니다. 데이터는 무손실 형식으로 캐시됩니다.
