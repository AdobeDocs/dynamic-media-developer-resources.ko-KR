---
title: 외부 이미지 소스
description: 이미지 제공은 외부 HTTP 및 FTP 서버의 소스 이미지에 대한 액세스를 지원합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90f96a76-e9f3-4ad0-84af-bc0d093acf19
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---

# 외부 이미지 소스{#foreign-image-sources}

이미지 제공은 외부 HTTP 및 FTP 서버의 소스 이미지에 대한 액세스를 지원합니다.

`src=` 또는 `mask=` 명령에 대한 외부 URL을 지정하려면 포함된 전체 URL을 중괄호로 구분하십시오.

` …&src={ *[!DNL foreignUrl]*}&…`

전체 절대 URL(`attribute::AllowDirectUrls`이(가) 설정된 경우) 및 `attribute::RootUrl`에 상대적인 URL이 허용됩니다. 절대 URL이 임베드되어 있고 특성: `AllowDirectUrls`이(가) 0이거나 상대 URL이 지정되어 있고 `attribute::RootUrl`이(가) 비어 있는 경우 오류가 발생합니다.

외부 이미지는 HTTP 응답에 포함된 캐싱 헤더에 따라 서버에 의해 캐시됩니다.
