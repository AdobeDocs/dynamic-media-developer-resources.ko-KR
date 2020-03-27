---
description: 하나 이상의 회사에 사용자 멤버십을 설정합니다.
seo-description: 하나 이상의 회사에 사용자 멤버십을 설정합니다.
seo-title: setCompanyMembership
solution: Experience Manager
title: setCompanyMembership
topic: Scene7 Image Production System API
uuid: 34c9d457-bc2e-4186-8a8f-50388410640a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setCompanyMembership{#setcompanymembership}

하나 이상의 회사에 사용자 멤버십을 설정합니다.

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
| ` *`userHandle`*` | `xsd:sting` | 아니요 | 사용자 핸들 |
| ` *`membershipArray`*` | `types:CompanyMembershipUpdateArray` | 예 | 다양한 회사 |

**출력(set 파섹**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

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
