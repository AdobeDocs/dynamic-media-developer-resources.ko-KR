---
description: 그룹을 삭제합니다.
solution: Experience Manager
title: deleteGroup
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0de188de-b4b6-4f48-9918-bcf962fa9482
TQID: 'https://experienceleague.adobe.com/skfJjk-dexrQR94ImWtaWV-1hkPmvrlFVn-EyA5mKtQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 86
ht-degree: 11%

---

# deleteGroup{#deletegroup}

그룹을 삭제합니다.

구문

## 승인된 사용자 유형 {#section-ebcc67723663494db0562275b1873460}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-42775102ec724c36ae5241eea1a00b8e}

**입력(deleteGroupParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 삭제할 그룹에 속한 회사에 대한 핸들입니다. |
| group핸들 | `xsd:string` | 예 | 삭제할 그룹에 대한 핸들입니다. |

**출력(deleteGroupParam)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-8f8501af3b3348a1b5701cf9622bf6e4}

이 샘플 코드는 회사에서 그룹을 삭제합니다. 이 작업에는 다른 작업에서 받아야 하는 그룹 핸들이 필요합니다.

**요청**

```java
<ns1:deleteGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>241</ns1:groupHandle>
</ns1:deleteGroupParam>
```

**응답**

없음.
