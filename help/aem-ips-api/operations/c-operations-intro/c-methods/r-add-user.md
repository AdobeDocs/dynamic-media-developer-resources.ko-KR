---
description: 사용자 계정을 만들고 하나 이상의 회사에 해당 계정을 추가합니다.
solution: Experience Manager
title: addUser
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: aed39e73-f528-4c26-8f62-c3d796e9101a
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 13%

---

# addUser{#adduser}

사용자 계정을 만들고 하나 이상의 회사에 해당 계정을 추가합니다.

여러 회사에 사용자를 추가할 때에서 회사 처리별로 해당 회사를 지정하십시오 `companyHandleArray`. 이 작업은 방금 추가한 사용자에게 핸들을 반환합니다.

## 승인된 사용자 유형 {#section-126ad42f844444fea11ecf8ad01fe1ec}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-40390a512e314b8d80ecffbb7729f6fb}

**입력(addUserParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| 이름 | `xsd:string` | 예 | 사용자의 이름입니다. |
| 성 | `xsd:string` | 예 | 사용자의 성입니다. |
| 이메일 | `xsd:string` | 예 | 사용자의 이메일 주소입니다. |
| 기본 역할 | `xsd:string` | 예 | 사용자가 속한 각 회사의 사용자에 대한 역할을 설정합니다. 그러나, `IpsAdmin` 역할은 다른 회사별 설정을 무시합니다. |
| 암호 | `xsd:string` | 예 | 사용자 암호 설정 |
| passwordExpires | `xsd:dateTime` | 아니요 | 암호 만료 기간을 설정합니다. 요청을 전달할 때 시간대를 제공합니다. 시간대는 중부 표준시로 조정됩니다. |
| isValid | `xsd:boolean` | 예 | 사용자가 유효한지 여부를 결정합니다. |
| membershipArray | `xsd:CompanyMembershipUpdateArray` | 예 | 회사 핸들의 배열입니다. |

**출력(addUserParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| 사용자 핸들 | `xsd:string` | 예 | 사용자의 핸들입니다. |

## 예제 {#section-2547cef622734b71919eef849960b5cb}

IPS API는 새 사용자를 지정하는 사용자 핸들 요소를 반환합니다.

**요청**

```java {.line-numbers}
<ns1:addUserParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:firstName>Joe</ns1:firstName>
   <ns1:lastName>User</ns1:lastName>
   <ns1:email>juser@adobe.com</ns1:email>
   <ns1:defaultRole>TrialSiteUser</ns1:role>
   <ns1:password>passw0rd</ns1:password>
   <ns1:isValid>true</ns1:isValid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:addUserParam>
```

**응답**

```java {.line-numbers}
<ns1:addUserReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>525s|juser@scene7.com</ns1:userHandle>
</ns1:addUserReturn>
```
