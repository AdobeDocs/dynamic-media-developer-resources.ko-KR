---
description: 회사 배열에서 사용자 멤버십을 가져옵니다.
seo-description: 회사 배열에서 사용자 멤버십을 가져옵니다.
seo-title: getCompanyMembership
solution: Experience Manager
title: getCompanyMembership
topic: Scene7 Image Production System API
uuid: fb3dfe29-4292-4ab2-8015-36c4930a9c05
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 16%

---


# getCompanyMembership{#getcompanymembership}

회사 배열에서 사용자 멤버십을 가져옵니다.

구문

## 인증된 사용자 유형 {#section-f8bba547e1f648648be99dc48fd72b5d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-8745c360c3e1400a88e9bdb26bcb93de}

**입력(getCompanyMembershipParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:string` | 아니요 | 획득하려는 멤버십에 속한 사용자의 핸들. |

**출력(getCompanyMembershipReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`membershipArray`*` | `types:CompanyMembershipArray` | 예 | 회사 멤버십의 배열입니다. |

## 예제 {#section-e4958d104ea344a4a79f57d07b46eba7}

이 코드 샘플은 사용자 핸들을 가져와 배열에 있는 사용자의 모든 회사 멤버십을 가져옵니다. 잠시 동안 응답이 잘렸습니다.

**요청**

```java
<ns1:getCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>70|kmagnusson@adobe.com</ns1:userHandle>
</ns1:getCompanyMembershipParam>
```

**응답**

```java
<getCompanyMembershipReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <membershipArray>
      <items>
         <companyHandle>48</companyHandle>
         <name>AIR</name>
         <rootPath>AIR/</rootPath>
         <expires>2101-01-31T23:00:00.485-08:00</expires>
      </items>
      ...
    </membershipArray>
</getCompanyMembershipReturn>
```

