---
description: 특정 회사의 사용자를 특정 그룹에 추가합니다.
solution: Experience Manager
title: addGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c03525e3-6bc4-4c6a-bb5b-b0cb2e6f6d0d
TQID: 'https://experienceleague.adobe.com/iwy99zQOP-peI6mJgDE8bp7NGN6bjH1g5MBN53gIkJw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 101
ht-degree: 10%

---

# addGroupMembers{#addgroupmembers}

특정 회사의 사용자를 특정 그룹에 추가합니다.

구문

## 승인된 사용자 유형 {#section-b4406c54ed7c4827be4c1acc957e0057}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-b28434dcf2ca4b4ea431136aac33913e}

**입력(addGroupMembersParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 회사 손잡이. |
| group핸들 | `xsd:string` | 예 | 그룹 핸들. |
| userHandleArray | `types:HandleArray` | 예 | 그룹에 추가하려는 사용자에 대한 핸들의 배열입니다. |

**출력(addGroupMembersParam)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-8f168b528aef4c4fa8c3d41f7686842f}

이 예제에서는 addGroupMembersParam을 사용하여 사용자를 단일 회사에 추가합니다. IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

**요청**

```java {.line-numbers}
<ns1:addGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
<ns1:userHandleArray><ns1:items>70|kmagnusson@adobe.com</ns1:items></ns1:userHandleArray>
</ns1:addGroupMembersParam>
```

**응답**

없음.

