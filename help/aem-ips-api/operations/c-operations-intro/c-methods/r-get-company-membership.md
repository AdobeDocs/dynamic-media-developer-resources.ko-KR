---
description: 회사 배열에서 사용자 멤버십을 가져옵니다.
solution: Experience Manager
title: getCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 53af8a97-208c-4c44-93d6-aa36a459af51
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 17%

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
| `*`userHandle`*` | `xsd:string` | 아니요 | 가져오려는 멤버십이 있는 사용자의 핸들입니다. |

**출력(getCompanyMembershipReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`membershipArray`*` | `types:CompanyMembershipArray` | 예 | 회사 멤버십의 배열입니다. |

## 예제 {#section-e4958d104ea344a4a79f57d07b46eba7}

이 코드 샘플은 사용자 핸들을 가져와서 사용자의 모든 회사 멤버십을 배열에 가져옵니다. 간결성을 위해 응답이 잘렸습니다.

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
