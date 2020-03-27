---
description: 하나 이상의 회사에 사용자를 추가합니다.
seo-description: 하나 이상의 회사에 사용자를 추가합니다.
seo-title: addCompanyMembership
solution: Experience Manager
title: addCompanyMembership
topic: Scene7 Image Production System API
uuid: be55041c-fc4e-46e8-bd2c-81b5931406f5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# addCompanyMembership{#addcompanymembership}

하나 이상의 회사에 사용자를 추가합니다.

구문

## 인증된 사용자 유형 {#section-ae926c7672984be79f6102748accab72}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-0e925b91d63e48aa91f0b0014e6a0cab}

**입력(addCompanyMembershipParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:string` | 아니요 | 멤버십을 추가할 사용자의 핸들 |
| ` *`membershipArray`*` | `types:CompanyMembershipUpdateArray` | 예 | 사용자를 추가하려는 여러 회사. |

**출력(addCompanyMembershipReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-5469f88bac7047cca131faa6b021e437}

이 예제에서는 ` *`companyHandleArray`*` 를 사용하여 사용자를 단일 회사에 추가합니다.

**요청**

```java
<ns1:addCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>621|jduvar@adobe.com</ns1:userHandle>
   <ns1:companyHandleArray>
      </ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:addCompanyMembershipParam>
```

**응답**

없음.
