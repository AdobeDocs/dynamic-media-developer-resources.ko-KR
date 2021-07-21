---
description: 실행하도록 예약된 작업입니다.
solution: Experience Manager
title: 예약된 작업
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c0084d10-ce38-4a01-9246-aaec44abc8eb
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 4%

---

# 예약된 작업{#scheduledjob}

실행하도록 예약된 작업입니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 회사 핸들. |
| `*`jobHandle`*` | `xsd:string` | 예약된 작업 핸들입니다. |
| `*`name`*` | `xsd:string` | 작업 이름. |
| `*`originalName`*` | `xsd:string` | 예약된 작업의 원래 이름입니다. |
| `*`type`*` | `xsd:string` | 작업 유형입니다. |
| `*`submitUserEmail`*` | `xsd:string` | 작업을 예약한 사용자의 이메일 주소입니다. |
| `*`로케일`*` | `xsd:string` | 작업 로그 세부 사항 및 전자 메일 지역화에 사용할 로케일입니다. 로케일은 `<language_code>[- <country_code>]`로 지정됩니다. 여기서 언어 코드는 ISO-639에서 지정한 소문자로 된 두 문자 코드이고 선택적 국가 코드는 ISO-3166에서 지정한 대문자인 두 문자 코드입니다. 예를 들어 영어(미국)의 로케일 문자열은 다음과 같습니다. `en-US` |
| `*`설명`*` | `xsd:string` | 원래 `submitJob`에 지정된 작업에 대한 설명입니다. |
| `*`execSchedule`*` | `xsd:string` | 작업이 실행되도록 예약된 경우입니다. |
| `*`nextFireTime`*` | `xsd:dateTime` | 작업을 실행할 날짜, 시간 및 시간대입니다. |
| `*`timeZone`*` | `xsd:dateTime` | 예약된 작업의 시간대입니다. |
| `*`triggerState`*` | `xsd:int` | 작업 트리거 상태 선택. |
| `*`imageServingPublishJob`*` | `types:ImageServingPublishJob` | 이미지 제공 게시 작업에 대한 작업 세부 사항입니다. |
| `*`imageServingRenderJob`*` | `types:ImageServingRenderJob` | 이미지 렌더링 작업에 대한 작업 세부 사항입니다. |
| `*`videoPublishJob`*` | `types:VideoPublishJob` | 비디오 게시 작업에 대한 작업 세부 사항입니다. [VideoPublishJob](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html)을 참조하십시오. |
| `*`serverDirectoryPublishJob`*` | `types:ServerDirectoryPublishJob` | 서버 디렉터리 게시 작업에 대한 작업 세부 정보입니다. |
| `*`uploadDirectoryJob`*` | `types:UploadDirectoryJob` | 업로드 디렉토리 작업에 대한 작업 세부 사항입니다. |
| `*`uploadUrlJob`*` | `types:UploadUrlsJob` | 업로드 URL 작업에 대한 작업 세부 사항입니다. |
| `*`optimizeImagesJob`*` | `types:OptimizeImagesJob` |  |
| `*`ripPdfJob`*` | `types:RipPdfsJob` |  |
| `*`reprocessAssetsJob`*` | `types:ReprocessAssetsJob` |  |
| `*`exportJob`*` | `types:ExportJob` | 이전에 업로드한 파일의 인증된 내보내기를 허용합니다. [내보내기 작업](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html)을 참조하십시오. |

## 주의 {#section-34ec157f281f412f9f0f6e861e6ed0cd}

`submitJob`에서 작업 유형 값을 지정하면 시스템이 해당 유형에 따라 작업을 반환합니다. 다음 작업을 반환할 수 있습니다.

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`
