---
description: 속성 집합 및 연결된 모든 속성을 삭제합니다.
solution: Experience Manager
title: deletePropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 72429030-200d-4e13-a537-10a728998a26
TQID: 'https://experienceleague.adobe.com/1j45J5Kw5P-3ba3WLNy9sTDBC5g4L17bynJQRaU5lAM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 83
ht-degree: 10%

---

# deletePropertySet{#deletepropertyset}

속성 집합 및 연결된 모든 속성을 삭제합니다.

구문

## 승인된 사용자 유형 {#section-b54aa8c854de400a989b4957412ff42c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-e5fc868f69494cf6858e03027db09101}

**입력(deletePropertySetParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| setHandle | `xsd:string` | 예 | 삭제할 속성 집합에 대한 핸들입니다. |

**출력(deletePropertySetParam)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-cf319fc8f86a40ab9cbd838b031973fe}

이 코드 샘플은 속성 집합을 삭제하기 위해 집합의 핸들을 IPS 웹 서비스 서버로 전송된 `deletePropertySetParam`의 필드로 사용합니다.

**요청**

```java
<deletePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</deletePropertySetParam>
```

**응답**

없음.

