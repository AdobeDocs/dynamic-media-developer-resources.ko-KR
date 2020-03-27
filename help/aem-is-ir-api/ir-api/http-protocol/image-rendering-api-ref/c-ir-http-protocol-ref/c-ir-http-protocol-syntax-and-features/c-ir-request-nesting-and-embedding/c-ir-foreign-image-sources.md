---
description: 이미지 제공은 외부 HTTP 및 FTP 서버에서 소스 이미지에 대한 액세스를 지원합니다.
seo-description: 이미지 제공은 외부 HTTP 및 FTP 서버에서 소스 이미지에 대한 액세스를 지원합니다.
seo-title: 외부 이미지 소스
solution: Experience Manager
title: 외부 이미지 소스
topic: Scene7 Image Serving - Image Rendering API
uuid: 28a17400-4807-4e14-937a-80309be53d55
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 외부 이미지 소스{#foreign-image-sources}

이미지 제공은 외부 HTTP 및 FTP 서버에서 소스 이미지에 대한 액세스를 지원합니다.

a `src=` 또는 `mask=` 명령의 외래 URL을 지정하려면중괄호로 포함된 전체 URL을 구분하면 됩니다.

` …&src={ *[!DNL foreignUrl]*}&…`

전체 절대 URL(설정된 경우) 및 관련 URL이 `attribute::AllowDirectUrls` `attribute::RootUrl` 허용됩니다. 절대 URL이 임베드되어 있고 다음과 같은 특성이 있는 경우 오류가 발생합니다.0이거나 상대 URL이 지정되어 있고 비어 `AllowDirectUrls` `attribute::RootUrl` 있는 경우

외부 이미지는 HTTP 응답에 포함된 캐싱 헤더에 따라 서버에서 캐시됩니다.
