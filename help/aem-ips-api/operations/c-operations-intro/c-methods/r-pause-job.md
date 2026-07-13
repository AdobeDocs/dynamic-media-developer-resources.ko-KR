---
description: 활성 작업을 일시 중지합니다.
solution: Experience Manager
title: pauseJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 010e969a-911e-49fc-8577-66c18cd4329c
TQID: 'https://experienceleague.adobe.com/7zMJW9fm8DiAPrO5cCDl87FhFMbgpw5NxoBHmIfEBog'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 61
ht-degree: 16%

---

# pauseJob{#pausejob}

활성 작업을 일시 중지합니다.

구문

## 승인된 사용자 유형 {#section-f2bf306ab4574871bd21f9f7dd681033}

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
| company핸들 | `xsd:string` | 예 | 회사를 위해 처리하십시오. |
| jobHandle | `xsd:string` | 예 | 일시 중지할 작업을 처리합니다. |

**출력(PauseJobReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

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

