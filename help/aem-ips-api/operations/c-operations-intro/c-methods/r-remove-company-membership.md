---
description: 하나 이상의 회사에서 사용자를 제거합니다.
solution: Experience Manager
title: removeCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1cb9a286-48a0-4542-a80a-c97fd973474e
TQID: 'https://experienceleague.adobe.com/5jjL8MnUtL046oSej3HErZB9hrD-ueEBC5-h9vD92HM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 10%

---

# removeCompanyMembership{#removecompanymembership}

하나 이상의 회사에서 사용자를 제거합니다.

구문

## 승인된 사용자 유형 {#section-e9a16c8a7d8d4845989a1488c9ca9c98}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-6dfce5e44d8a4799afd0c231a0b10463}

**입력(removeCompanyMembershipParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| 사용자 핸들 | `xsd:string` | 아니요 | 제거할 멤버십이 있는 사용자의 핸들입니다. |
| companyHandleArray | `types:HandleArray` | 예 | 사용자를 제거할 회사의 핸들입니다. |

**출력(removeCompanyMembershipReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-6b7903195e8647a1bd0502f87387ca62}

이 코드 샘플은 회사에서 사용자를 제거합니다. 선택적 사용자 핸들을 생략하여 회사 핸들 배열에 지정된 회사에서 모든 사용자를 제거합니다.

**요청**

```java
<ns1:removeCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>621|jduvar@adobe.com</ns1:userHandle>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:removeCompanyMembershipParam>
```

**응답**

없음.

