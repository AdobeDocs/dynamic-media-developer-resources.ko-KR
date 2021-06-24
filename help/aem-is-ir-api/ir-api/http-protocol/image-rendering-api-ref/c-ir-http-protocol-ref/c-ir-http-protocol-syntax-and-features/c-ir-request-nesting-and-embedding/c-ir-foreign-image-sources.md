---
description: 이미지 제공 서비스는 외부 HTTP 및 FTP 서버에서 소스 이미지에 대한 액세스를 지원합니다.
solution: Experience Manager
title: 외부 이미지 소스
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 90f96a76-e9f3-4ad0-84af-bc0d093acf19
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# 외부 이미지 소스{#foreign-image-sources}

이미지 제공 서비스는 외부 HTTP 및 FTP 서버에서 소스 이미지에 대한 액세스를 지원합니다.

`src=` 또는 `mask=` 명령의 외부 URL을 지정하려면포함된 전체 URL은 중괄호로 구분하면 됩니다.

` …&src={ *[!DNL foreignUrl]*}&…`

전체 절대 URL(`attribute::AllowDirectUrls`이 설정된 경우) 및 `attribute::RootUrl`에 상대적인 URL이 허용됩니다. 절대 URL이 포함된 경우 및 속성이 다음과 같이 발생하는 경우 오류가 발생합니다.`AllowDirectUrls`은 0이거나 상대 URL이 지정되어 있고 `attribute::RootUrl`이 비어 있는 경우 입니다.

외부 이미지는 HTTP 응답에 포함된 캐싱 헤더에 따라 서버에서 캐시됩니다.
