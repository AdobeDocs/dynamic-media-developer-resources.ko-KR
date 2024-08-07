---
description: 그룹 배열에서 사용자를 제거합니다.
solution: Experience Manager
title: removeGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 892ee01c-e07b-4321-b0b7-5bb606036340
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 8%

---

# removeGroupMembership{#removegroupmembership}

그룹 배열에서 사용자를 제거합니다.

**제거 명령의 차이점**

* `removeGroupMembers`: 그룹에서 여러 사용자를 제거합니다.
* `removeGroupMembership`: 그룹 배열에서 개별 사용자를 제거합니다.

## 승인된 사용자 유형 {#section-83f3048bbe5a4f62b7b14dc9efdd951a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-d6a15fa70d3d4fc69da200cdaf59904e}

**입력(removeGroupMembershipParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| 사용자 핸들 | `xsd:string` | 아니요 | 그룹 구성원을 제거할 회사에 대한 핸들입니다. |
| groupHandleArray | `types:HandleArray` | 예 | 회사를 제거할 그룹의 핸들 배열입니다. |

**출력(removeGroupMembershipReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-f8d4181170a243efb9faf5824ae96197}

이 코드 샘플은 그룹에서 사용자를 제거합니다.

**요청**

```java
<ns1:removeGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>47</ns1:userHandle>
   <ns1:groupHandleArray>
      <ns1:items>225</ns1:items>
   </ns1:groupHandleArray>
</ns1:removeGroupMembershipParam>
```

**응답**

없음.
