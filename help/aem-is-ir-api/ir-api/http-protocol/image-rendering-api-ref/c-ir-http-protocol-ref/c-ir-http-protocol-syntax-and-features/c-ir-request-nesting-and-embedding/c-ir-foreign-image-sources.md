---
title: 외부 이미지 소스
description: 이미지 제공은 외부 HTTP 및 FTP 서버의 소스 이미지에 대한 액세스를 지원합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90f96a76-e9f3-4ad0-84af-bc0d093acf19
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---

# 외부 이미지 소스{#foreign-image-sources}

이미지 제공은 외부 HTTP 및 FTP 서버의 소스 이미지에 대한 액세스를 지원합니다.

에 대한 외부 URL을 지정하려면 `src=` 또는 `mask=` 명령, 포함된 전체 URL은 중괄호로 구분하십시오.

` …&src={ *[!DNL foreignUrl]*}&…`

전체 절대 URL(다음의 경우) `attribute::AllowDirectUrls` (설정됨) 및 URL이 `attribute::RootUrl` 허용됩니다. 절대 URL이 포함되고 속성이 다음과 같은 경우 오류가 발생합니다. `AllowDirectUrls` 은 0이거나, 상대 URL이 지정된 경우 이고 `attribute::RootUrl` 은(는) 비어 있습니다.

외부 이미지는 HTTP 응답에 포함된 캐싱 헤더에 따라 서버에 의해 캐시됩니다.
