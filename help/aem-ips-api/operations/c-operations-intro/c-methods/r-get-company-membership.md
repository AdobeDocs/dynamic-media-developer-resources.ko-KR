---
description: 회사 배열에서 사용자의 멤버십을 가져옵니다.
solution: Experience Manager
title: getCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 53af8a97-208c-4c44-93d6-aa36a459af51
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 18%

---

# getCompanyMembership{#getcompanymembership}

회사 배열에서 사용자의 멤버십을 가져옵니다.

구문

## 승인된 사용자 유형 {#section-f8bba547e1f648648be99dc48fd72b5d}

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
| 사용자 핸들 | `xsd:string` | 아니요 | 멤버십을 가져올 사용자의 핸들입니다. |

**출력(getCompanyMembershipReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| membershipArray | `types:CompanyMembershipArray` | 예 | 회사 멤버십 배열. |

## 예제 {#section-e4958d104ea344a4a79f57d07b46eba7}

이 코드 샘플은 사용자 핸들을 가져와 배열에서 사용자의 모든 회사 멤버십을 가져옵니다. 간결성을 위해 응답이 잘렸습니다.

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
