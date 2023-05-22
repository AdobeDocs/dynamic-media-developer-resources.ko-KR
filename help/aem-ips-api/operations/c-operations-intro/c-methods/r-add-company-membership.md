---
description: 하나 이상의 회사에 사용자를 추가합니다.
solution: Experience Manager
title: addCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6efef4fb-f2e5-4c41-b739-a36ac2f17884
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 14%

---

# addCompanyMembership{#addcompanymembership}

하나 이상의 회사에 사용자를 추가합니다.

구문

## 승인된 사용자 유형 {#section-ae926c7672984be79f6102748accab72}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-0e925b91d63e48aa91f0b0014e6a0cab}

**입력(addCompanyMembershipParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| 사용자 핸들 | `xsd:string` | 아니요 | 멤버십을 추가하려는 사용자에 대한 핸들입니다. |
| membershipArray | `types:CompanyMembershipUpdateArray` | 예 | 사용자를 추가하는 회사의 배열입니다. |

**출력(addCompanyMembershipReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-5469f88bac7047cca131faa6b021e437}

이 예제에서는 companyHandleArray를 사용하여 사용자를 단일 회사에 추가합니다.

**요청**

```javascript {.line-numbers}
<ns1:addCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>621|jduvar@adobe.com</ns1:userHandle>
   <ns1:companyHandleArray>
      </ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:addCompanyMembershipParam>
```

**응답**

없음.
