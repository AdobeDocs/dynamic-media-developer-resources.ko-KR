---
description: 확대/축소 대상을 삭제합니다.
solution: Experience Manager
title: deleteZoomTarget
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa1f7cf8-038a-4fa8-b869-12ce4b2ad41f
TQID: 'https://experienceleague.adobe.com/dAO3kI0G4UM6HHSwWTqJLb0cS4gkfZi-pR-CAbknUe4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 81
ht-degree: 11%

---

# deleteZoomTarget{#deletezoomtarget}

확대/축소 대상을 삭제합니다.

## 승인된 사용자 유형 {#section-09ca82bc817e49048271c5cba545702e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>사용자에게 에셋에 대한 읽기 및 쓰기 권한이 있어야 합니다.

## 매개 변수 {#section-225330a45e7a408f8375e084677d9cb1}

**입력(deleteZoomTargetParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 확대/축소 대상이 속한 회사에 대한 핸들입니다. |
| 확대/축소 대상 핸들 | `xsd:string` | 예 | 삭제할 확대/축소 대상에 대한 핸들입니다. |

**출력(deleteZoomTargetParam)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예 {#section-a35857a5ca884357a879f7ba6cf985fe}

이 코드 샘플은 회사에서 확대/축소 대상을 삭제합니다.

**요청**

```java
<ns1:deleteZoomTargetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:zoomTargetHandle>34194|9|301</ns1:zoomTargetHandle>
</ns1:deleteZoomTargetParam>
```

**응답**

없음.
