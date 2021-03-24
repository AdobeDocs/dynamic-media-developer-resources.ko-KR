---
description: 이미지 제공은 외부 HTTP 및 FTP 서버에서 소스 이미지에 대한 액세스를 지원합니다.
solution: Experience Manager
title: 외부 이미지 소스
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---


# 외부 이미지 소스{#foreign-image-sources}

이미지 제공은 외부 HTTP 및 FTP 서버에서 소스 이미지에 대한 액세스를 지원합니다.

`src=` 또는 `mask=` 명령에 대한 외래 URL을 지정하려면중괄호로 포함된 전체 URL을 구분하면 됩니다.

` …&src={ *[!DNL foreignUrl]*}&…`

전체 절대 URL(`attribute::AllowDirectUrls`이 설정된 경우) 및 `attribute::RootUrl`에 상대적인 URL이 허용됩니다. 절대 URL이 포함되고 다음과 같은 특성이 있는 경우 오류가 발생합니다.`AllowDirectUrls`은 0이거나 상대 URL이 지정되고 `attribute::RootUrl`이(가) 비어 있는 경우

외부 이미지는 HTTP 응답에 포함된 캐싱 헤더에 따라 서버에서 캐시됩니다.
