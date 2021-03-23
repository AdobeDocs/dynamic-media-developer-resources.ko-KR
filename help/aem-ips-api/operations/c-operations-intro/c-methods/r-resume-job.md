---
description: 일시 중지된 작업을 다시 시작합니다.
seo-description: 일시 중지된 작업을 다시 시작합니다.
seo-title: resumeJob
solution: Experience Manager
title: resumeJob
uuid: 0ca5db75-cce0-4afc-9a58-c47c6229931e
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 15%

---


# resumeJob{#resumejob}

일시 중지된 작업을 다시 시작합니다.

구문

## 인증된 사용자 유형 {#section-eab49f4b6d1041179000326a10fee889}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-6b2f8aa65d4d4ae1af0c9cee468b0a51}

**입력(resumeJobParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 다시 시작할 작업이 있는 회사에 대한 핸들입니다. |
| `*`jobHandle`*` | `xsd:string` | 예 | 일시 중지된 작업의 핸들입니다. |

**출력(resumeJobReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-d0524e031f1f43d89430eade19526162}

이 코드 샘플은 일시 중지된 작업을 다시 시작합니다.

**요청**

```java
<resumeJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</resumeJobParam>
```

**응답**

없음.
