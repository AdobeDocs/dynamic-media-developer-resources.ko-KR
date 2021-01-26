---
description: 회사 취급에 의해 지정된 회사의 사용자를 반환합니다.
seo-description: 회사 취급에 의해 지정된 회사의 사용자를 반환합니다.
seo-title: getCompanyMembers
solution: Experience Manager
title: getCompanyMembers
topic: Dynamic Media Image Production System API
uuid: 45e2d040-a70a-46f4-863a-633ddabcbcf6
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 15%

---


# getCompanyMembers{#getcompanymembers}

회사 취급에 의해 지정된 회사의 사용자를 반환합니다.

구문

## 인증된 사용자 유형 {#section-b2bc2fa0cc944cea8be82524838307cc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-5602e4d6f2214e398e6a804e61f1a088}

**입력(getCompanyMembersParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 얻고자 하는 구성원이 있는 회사에 대한 핸들입니다. |
| `*`includeInvalid`*` | `xsd:boolean` | 예 | 잘못된 회사 포함. |

**출력(getCompanyMembersReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`memberArray`*` | `types:CompanyMemberArray` | 예 | 사용자 멤버십 배열입니다. |

## 예제 {#section-39d8cf3653fd4fe8b842caabac9dedfc}

이 코드 샘플은 사용자 배열에 있는 회사의 모든 구성원을 반환합니다. 잠시 동안 응답이 잘렸습니다.

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

