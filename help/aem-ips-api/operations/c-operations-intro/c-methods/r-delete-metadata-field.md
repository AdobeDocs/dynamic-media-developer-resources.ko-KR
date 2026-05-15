---
description: 회사의 메타데이터 필드를 삭제합니다.
solution: Experience Manager
title: deleteMetadataField
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1922fc1b-2abc-4d31-985a-65c788af4d46
TQID: 'https://experienceleague.adobe.com/GnKkb-vTCdD5PwU111sxefzxR7FN74hk3i66c3gcH9I'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 99
ht-degree: 9%

---

# deleteMetadataField{#deletemetadatafield}

회사의 메타데이터 필드를 삭제합니다.

구문

## 승인된 사용자 유형 {#section-63e7d17f4b434995a872838bfff7f9ff}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-73f12a30cc4340b6b32dd11effd5195e}

**입력(deleteMetadataFieldParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 삭제할 메타데이터 필드가 포함된 회사에 대한 핸들입니다. |
| 필드 핸들 | `xsd:string` | 예 | 삭제할 메타데이터 필드에 대한 핸들입니다. |

**출력(deleteMetadataFieldParam)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-e1c474ea91a040609ecd7c2400f4fa3c}

이 코드 샘플은 회사의 메타데이터 필드를 삭제합니다. 회사 핸들과 메타데이터 핸들을 IPS 웹 서비스 서버에 전달된 `deleteMetadataFieldParam`의 필드로 사용하여 이 작업을 수행합니다.

**요청**

```java
<deleteMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
</deleteMetadataFieldParam>
```

**응답**

없음.0
