---
description: 특정 그룹에서 회사 사용자를 제거합니다.
solution: Experience Manager
title: removeGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8a9b7d54-d11b-41a8-9783-573a316e0ac6
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 9%

---

# removeGroupMembers{#removegroupmembers}

특정 그룹에서 회사 사용자를 제거합니다.

**제거 명령 간의 차이**

* `removeGroupMembers`: 그룹에서 여러 사용자를 제거합니다.
* `removeGroupMembership`: 그룹 배열에서 개별 사용자를 제거합니다.

## 인증된 사용자 유형 {#section-2c64cdac15184fbba6c7b2945b5d87f7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-b5596614a3be4ce5962455884e4636af}

**입력(removeGroupMembersParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 함께 작업할 사용자와 회사의 핸들입니다. |
| `*`groupHandle`*` | `xsd:string` | 예 | 그룹 핸들. |
| `*`userHandleArray`*` | `types:HandleArray` | 예 | 그룹 멤버십을 제거하려는 사용자를 위한 일련의 핸들입니다. |

**출력(removeGroupMembersParam)**

IPS API가 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-9eedac852cea46ec80de6a6928bf97ac}

이 코드 샘플은 지정된 회사에서 사용자를 제거합니다. 사용자 핸들 배열을 사용하는 그룹에서 여러 사용자를 제거합니다.

**요청**

```java
<ns1:removeGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
   <ns1:userHandleArray>
      <ns1:items>621|jduvar@adobe.com</ns1:items>
   </ns1:userHandleArray>
</ns1:removeGroupMembersParam>
```

**응답**

없음.
