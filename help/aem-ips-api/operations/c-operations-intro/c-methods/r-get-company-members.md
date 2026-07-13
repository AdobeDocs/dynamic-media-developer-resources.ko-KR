---
description: 회사 핸들에 의해 지정된 회사의 사용자를 반환합니다.
solution: Experience Manager
title: getCompanyMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: da5e5a48-2e0b-4ccc-a71e-b5b746484d4a
TQID: 'https://experienceleague.adobe.com/QMJGqj7IEplTMdFFwVP3UReZAJsi25tHaaMewM30MSU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 89
ht-degree: 15%

---

# getCompanyMembers{#getcompanymembers}

회사 핸들에 의해 지정된 회사의 사용자를 반환합니다.

구문

## 승인된 사용자 유형 {#section-b2bc2fa0cc944cea8be82524838307cc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-5602e4d6f2214e398e6a804e61f1a088}

**입력(getCompanyMembersParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 멤버를 가져오려는 회사에 대한 핸들. |
| includeInvalid | `xsd:boolean` | 예 | 잘못된 회사를 포함합니다. |

**출력(getCompanyMembersReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| memberArray | `types:CompanyMemberArray` | 예 | 사용자 멤버십 배열. |

## 예제 {#section-39d8cf3653fd4fe8b842caabac9dedfc}

이 코드 샘플은 사용자 배열에 있는 회사의 모든 멤버를 반환합니다. 간결성을 위해 응답이 잘렸습니다.

**요청**

```java
<ns1:getCompanyMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:includeInvalid>false</ns1:includeInvalid>
</ns1:getCompanyMembersParam>
```

**응답**

```java
<getCompanyMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <memberArray>
      <items>
         <userHandle>66|pbayol@adobe.com</userHandle>
         <firstName>Peter</firstName>
         <lastName>Bayol</lastName>
         <email>pbayol@adobe.com</email>
         <role>IpsAdmin</role>
         <isValid>true</isValid>
         <passwordExpires>2107-07-25T23:12:49.472-07:00</passwordExpires>
      </items>
      ...
   </memberArray>
</getCompanyMembersReturn>
```

