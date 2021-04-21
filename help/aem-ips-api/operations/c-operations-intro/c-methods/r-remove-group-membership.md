---
description: 그룹 배열에서 사용자를 제거합니다.
solution: Experience Manager
title: removeGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 10%

---


# removeGroupMembership{#removegroupmembership}

그룹 배열에서 사용자를 제거합니다.

**제거 명령 간 차이**

* `removeGroupMembers`:그룹에서 여러 사용자를 제거합니다.
* `removeGroupMembership`:그룹 배열에서 개별 사용자를 제거합니다.

## 인증된 사용자 유형 {#section-83f3048bbe5a4f62b7b14dc9efdd951a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-d6a15fa70d3d4fc69da200cdaf59904e}

**입력(removeGroupMembershipParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | 아니요 | 그룹 구성원을 제거하려는 회사의 핸들입니다. |
| `*`groupHandleArray`*` | `types:HandleArray` | 예 | 회사를 제거할 그룹에 대한 핸들 배열입니다. |

**출력(removeGroupMembershipReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-f8d4181170a243efb9faf5824ae96197}

이 코드 샘플은 사용자를 그룹에서 제거합니다.

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
