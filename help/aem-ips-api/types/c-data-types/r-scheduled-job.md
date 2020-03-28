---
description: 실행되도록 예약된 작업.
seo-description: 실행되도록 예약된 작업.
seo-title: 예약작업
solution: Experience Manager
title: 예약작업
topic: Scene7 Image Production System API
uuid: cf0db523-2138-48c6-abbd-460a961e7de1
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

---


# 예약작업{#scheduledjob}

실행되도록 예약된 작업.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 회사 핸들 |
| ` *`jobHandle`*` | `xsd:string` | 예약된 작업 핸들 |
| ` *`name`*` | `xsd:string` | 작업 이름. |
| ` *`originalName`*` | `xsd:string` | 예약된 작업의 원래 이름입니다. |
| ` *`type`*` | `xsd:string` | 작업 유형. |
| ` *`submitUserEmail`*` | `xsd:string` | 작업을 예약한 사용자의 이메일 주소입니다. |
| ` *`로케일`*` | `xsd:string` | 작업 로그 세부 사항 및 이메일 현지화에 사용할 로케일입니다. 로케일은 언어 코드가 ISO-639에서 지정한 소문자, 두 문자 코드인 소문자, 그리고 선택적 국가 코드는 ISO-3166에서 지정한 대소문자, 두 문자 코드인 경우 로 지정됩니다. `<language_code>[- <country_code>]` 예를 들어 영어(미국)의 로케일 문자열은 다음과 같습니다. `en-US`Adobe |
| ` *`description`*` | `xsd:string` | 에 원래 지정된 작업에 대한 `submitJob`설명입니다. |
| ` *`execSchedule`*` | `xsd:string` | 작업이 실행되도록 예약된 경우. |
| ` *`nextFireTime`*` | `xsd:dateTime` | 작업을 실행할 날짜, 시간 및 표준 시간대 |
| ` *`timeZone`*` | `xsd:dateTime` | 예약된 작업의 시간대입니다. |
| ` *`triggerState`*` | `xsd:int` | 작업 트리거 상태 선택 |
| ` *`imageServingPublishJob`*` | `types:ImageServingPublishJob` | 이미지 제공 게시 작업에 대한 작업 세부 정보입니다. |
| ` *`imageServingRenderJob`*` | `types:ImageServingRenderJob` | 이미지 렌더링 작업에 대한 작업 세부 정보입니다. |
| ` *`videoPublishJob`*` | `types:VideoPublishJob` | 비디오 게시 작업의 작업 세부 정보입니다. VideoPublishJob [을 참조하십시오](https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_scheduled_job.html). |
| ` *`serverDirectoryPublishJob`*` | `types:ServerDirectoryPublishJob` | 서버 디렉토리 게시 작업에 대한 작업 세부 정보입니다. |
| ` *`uploadDirectoryJob`*` | `types:UploadDirectoryJob` | 업로드 디렉토리 작업에 대한 작업 세부 정보입니다. |
| ` *`uploadUrlJob`*` | `types:UploadUrlsJob` | 업로드 URL 작업에 대한 작업 세부 정보입니다. |
| ` *`optimizeImagesJob`*` | `types:OptimizeImagesJob` |  |
| ` *`ripPdfsJob`*` | `types:RipPdfsJob` |  |
| ` *`reprocessAssetsJob`*` | `types:ReprocessAssetsJob` |  |
| ` *`exportJob`*` | `types:ExportJob` | 이전에 업로드한 파일의 인증된 내보내기를 허용합니다. 내보내기 [작업을 참조하십시오](https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_scheduled_job.html). |

## 주의 {#section-34ec157f281f412f9f0f6e861e6ed0cd}

에서 작업 유형 값을 지정하면 `submitJob`해당 유형을 기반으로 작업이 반환됩니다. 다음 작업을 반환할 수 있습니다.

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`

