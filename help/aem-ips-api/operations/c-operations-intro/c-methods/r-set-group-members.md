---
description: 특정 회사에 속한 사용자의 그룹 멤버십을 설정합니다.
solution: Experience Manager
title: setGroupMember
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81348da7-6733-4da9-8a0a-376fccf791ea
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 9%

---

# setGroupMember{#setgroupmembers}

특정 회사에 속한 사용자의 그룹 멤버십을 설정합니다.

이 작업을 수행할 수 있는 권한이 없는 경우 작업에 인증 오류가 발생합니다. 이는 사용자 핸들 배열의 사용자 중 회사 핸들에 지정된 회사에 속하지 않는 사용자가 있는 경우에도 마찬가지입니다.

## 승인된 사용자 유형 {#section-4523594039c24aa29c8d0d5c9c415391}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-6a18562fc8e942af94be10bbb8c51151}

**입력(setGroupMembersParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 회사 핸들. |
| group핸들 | `xsd:string` | 예 | 그룹 핸들. |
| userHandleArray | `types:HandleArray` | 예 | 설정할 그룹 멤버십의 사용자 핸들 배열입니다. |

**출력(setGroupMembesReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-9c528c3f44a141ce9eaddf634f26c487}

이 코드 샘플은 단일 사용자에 대한 그룹 멤버십을 설정합니다.

**요청**

```java
<ns1:setGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
   <ns1:userHandleArray>
      <ns1:items>70|kmagnusson@adobe.com</ns1:items>
   </ns1:userHandleArray>
</ns1:setGroupMembersParam>
```

**응답**

없음.
