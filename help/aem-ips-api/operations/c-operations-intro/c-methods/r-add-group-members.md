---
description: 특정 회사의 사용자를 특정 그룹에 추가합니다.
seo-description: 특정 회사의 사용자를 특정 그룹에 추가합니다.
seo-title: addGroupMembers
solution: Experience Manager
title: addGroupMembers
topic: Scene7 Image Production System API
uuid: 382d36a8-7c93-48e6-a54b-425c5e6414fe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 11%

---


# addGroupMembers{#addgroupmembers}

특정 회사의 사용자를 특정 그룹에 추가합니다.

구문

## 인증된 사용자 유형 {#section-b4406c54ed7c4827be4c1acc957e0057}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-b28434dcf2ca4b4ea431136aac33913e}

**입력(addGroupMembersParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 예 | 회사의 손잡이입니다. |
| ` *`groupHandle`*` | `xsd:string` | 예 | 그룹 핸들. |
| ` *`userHandleArray`*` | `types:HandleArray` | 예 | 그룹에 추가하려는 사용자에 대한 핸들 배열입니다. |

**출력(addGroupMembersParam)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-8f168b528aef4c4fa8c3d41f7686842f}

이 예에서는 ` *`addGroupMembersParam`*`을 사용하여 사용자를 단일 회사에 추가합니다. IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

**요청**

```java
<ns1:addGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
<ns1:userHandleArray><ns1:items>70|kmagnusson@adobe.com</ns1:items></ns1:userHandleArray>
</ns1:addGroupMembersParam>
```

**응답**

없음.
