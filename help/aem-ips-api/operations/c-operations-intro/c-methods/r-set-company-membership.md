---
description: 하나 이상의 회사에 사용자 구성원을 설정합니다.
solution: Experience Manager
title: setCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 43144c75-1d83-4e1d-8319-c3275d349a2f
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 14%

---

# setCompanyMembership{#setcompanymembership}

하나 이상의 회사에 사용자 구성원을 설정합니다.

구문

## 인증된 사용자 유형 {#section-0cbcc78cfee64c2baf66f29cce6d0a65}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-3930dc6a016140178631083563598104}

**입력(setCompanyMembershipParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`userHandle`*` | `xsd:sting` | 아니요 | 사용자 핸들. |
| `*`membershipArray`*` | `types:CompanyMembershipUpdateArray` | 예 | 기업의 배열입니다. |

**출력(setCompanyMembershipParam)**

IPS API가 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-862c0cc32ce0407ab248028e690a8386}

이 코드 샘플은 사용자를 회사에 추가합니다. 필요한 경우 회사 핸들 어레이에 여러 회사를 지정합니다.

**요청**

```java
<ns1:setCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>3341|juser@scene7.com</ns1:userHandle>
   <ns1:companyHandleArray>
      <ns1:items>137</ns1:items>
   </ns1:companyHandleArray>
</ns1:setCompanyMembershipParam>
```

**응답**

없음.
