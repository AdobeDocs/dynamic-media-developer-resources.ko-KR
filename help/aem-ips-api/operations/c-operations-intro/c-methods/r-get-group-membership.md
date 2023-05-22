---
description: 그룹의 멤버를 반환합니다.
solution: Experience Manager
title: getGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 847e4982-219d-47fd-b94c-f7d520ba1367
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 20%

---

# getGroupMembership{#getgroupmembership}

그룹의 멤버를 반환합니다.

구문

## 승인된 사용자 유형 {#section-35d070e5c4d74ca69df508368953cfb8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-2e92f850254e46e48403acaa215341a5}

**입력(getGroupMembershipParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| 사용자 핸들 | `xsd:string` | 아니요 | 사용자의 핸들입니다. |
| company핸들 | `xsd:string` | 아니요 | 회사 손잡이. |

**출력(getGroupMembershipReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| groupArray | `types:GroupArray` | 예 | 그룹 배열. |

## 예제 {#section-ebb437369f4f4487b3eb2ef0c078b8ae}

이 코드 샘플은 그룹의 모든 멤버를 반환합니다. 회사 및 사용자 핸들은 선택 사항이므로 이 작업은 모든 그룹의 모든 구성원을 반환할 수 있습니다.

**요청**

```java
<ns1:getGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getGroupMembershipParam>
```

**응답**

```java
<getGroupMembershipReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupArray>
      <items>
         <groupHandle>225</groupHandle><companyHandle>47</companyHandle><name>MyGroup</name><isSystemDefined>false</isSystemDefined></items></groupArray></getGroupMembershipReturn>
```
