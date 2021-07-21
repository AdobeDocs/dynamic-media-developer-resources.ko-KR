---
description: 활성 작업을 일시 중지합니다.
solution: Experience Manager
title: pauseJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 010e969a-911e-49fc-8577-66c18cd4329c
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 18%

---

# pauseJob{#pausejob}

활성 작업을 일시 중지합니다.

구문

## 인증된 사용자 유형 {#section-f2bf306ab4574871bd21f9f7dd681033}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-7aedb924cf8b4e05a0dc927636d537a0}

**입력(pauseJobParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 회사를 담당합니다. |
| `*`jobHandle`*` | `xsd:string` | 예 | 일시 중지할 작업을 처리합니다. |

**출력(PauseJobReturn)**

IPS API가 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-ee4914f9496f4bd88556728a48fb22c1}

이 코드 샘플은 활성 작업을 일시 중지합니다.

**요청**

```java
<pauseJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</pauseJobParam>
```

**응답**

없음.
