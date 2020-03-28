---
description: 그룹의 구성원을 반환합니다.
seo-description: 그룹의 구성원을 반환합니다.
seo-title: getGroupMembership
solution: Experience Manager
title: getGroupMembership
topic: Scene7 Image Production System API
uuid: 5ec48e8c-378b-43a3-b3dc-aa21dbf339b5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getGroupMembership{#getgroupmembership}

그룹의 구성원을 반환합니다.

구문

## 인증된 사용자 유형 {#section-35d070e5c4d74ca69df508368953cfb8}

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
| ` *`userHandle`*` | `xsd:string` | 아니요 | 사용자에 대한 핸들입니다. |
| ` *`companyHandle`*` | `xsd:string` | 아니요 | 회사의 손잡이입니다. |

**출력(getGroupMembershipReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`groupArray`*` | `types:GroupArray` | 예 | 그룹 배열. |

## 예제 {#section-ebb437369f4f4487b3eb2ef0c078b8ae}

이 코드 샘플은 그룹의 모든 멤버를 반환합니다. 회사 및 사용자 핸들은 선택 사항이기 때문에 작업은 모든 그룹의 모든 구성원을 반환할 수 있습니다.

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

