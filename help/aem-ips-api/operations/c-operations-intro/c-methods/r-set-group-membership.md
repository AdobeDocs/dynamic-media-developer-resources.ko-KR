---
description: 사용자의 그룹 멤버십을 설정합니다.
solution: Experience Manager
title: setGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0a355a34-1c2d-48c1-ba12-7d07d1673d09
TQID: 'https://experienceleague.adobe.com/j-wK2g-evSRY0YD3ZspgT--giCkKJl1VBYgPylixVz8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 96
ht-degree: 11%

---

# setGroupMembership{#setgroupmembership}

사용자의 그룹 멤버십을 설정합니다.

구문

## 승인된 사용자 유형 {#section-3d6308a8a5694ed085e04d1c37982b9e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-6aeda13b26af4796aad1306ac7a9ad17}

**입력(setGroupMembershipParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| 사용자 핸들 | `xsd:string` | 아니요 | 그룹 멤버십을 설정할 사용자에 대한 핸들입니다. |
| company핸들 | `xsd:string` | 아니요 | 회사 핸들. |
| groupHandleArray | `types:HandleArray` | 예 | 사용자가 속한 그룹에 대한 핸들의 배열입니다. |

**출력(setGroupMembershipReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-67b86d259df24938896fe19061845811}

이 코드 샘플은 사용자를 그룹의 구성원으로 만듭니다. 그룹 핸들 배열로 여러 그룹에 사용자를 추가합니다.

**요청**

```java
<ns1:setGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>70|kmagnusson@adobe.com</ns1:userHandle>
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray>
      <ns1:items>225</ns1:items>
   </ns1:groupHandleArray>
</ns1:setGroupMembershipParam>
```

**응답**

없음.

