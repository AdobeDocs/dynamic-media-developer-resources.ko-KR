---
description: 진행 중인 작업을 중지합니다.
seo-description: 진행 중인 작업을 중지합니다.
seo-title: stopJob
solution: Experience Manager
title: stopJob
topic: Dynamic Media Image Production System API
uuid: 698c1652-5afa-4a2c-819a-1ba6ffc6aacf
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 20%

---


# stopJob{#stopjob}

진행 중인 작업을 중지합니다.

구문

## 인증된 사용자 유형 {#section-b222f561143747f6ad089aadc0b274d8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-2b64f074e37c4c38849994f3bc65342a}

**입력(stopJobParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 회사 핸들. |
| `*`jobHandle`*` | `xsd:string` | 예 | 중지할 작업을 처리합니다. |

**출력(stopJobReturn0**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-f7e07fa09ae24dc89685533f20ab3b81}

**요청**

```java
<stopJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</stopJobParam>
```

**응답**

없음.
