---
description: '사용자 속성(예: 이름, 이메일, 역할 등)을 설정합니다.'
solution: Experience Manager
title: setUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d8f8fe53-a874-4b77-9084-9a369862a672
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 15%

---

# setUserInfo{#setuserinfo}

사용자 속성(예: 이름, 이메일, 역할 등)을 설정합니다.

구문

## 승인된 사용자 유형 {#section-6c28db5d15b3449492a73749e4f981ac}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-71b457921fe74acb862a1e112e550211}

**입력(setUserInfoParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| 사용자 핸들 | `xsd:string` | 아니요 | 사용자 핸들. |
| 이름 | `xsd:string` | 예 | 이름. |
| 성 | `xsd:string` | 예 | 성. |
| 이메일 | `xsd:string` | 예 | 사용자 이메일. |
| 기본 역할 | `xsd:string` | 예 | 사용자가 속한 각 회사의 사용자에 대한 역할을 설정합니다. 그러나 `IpsAdmin` 역할은 다른 회사별 설정을 무시합니다. |
| passwordExpires | `xsd:dateTime` | 아니요 | 의 암호 만료일을 설정합니다. |
| isValid | `xsd:boolean` | 예 | 사용자가 유효한 IPS 사용자인지 확인합니다. |
| membershipArray | `types:CompanyMembershipUpdateArray` | 예 | 회사 핸들의 배열입니다. |

**출력(setUserInfoReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-272c103076fb4de0a53729e2f6bfb895}

**요청**

```java
<setUserInfoParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <firstName>test</firstName>
   <lastName>test</lastName>
   <email>test@test.test</email>
   <defaultRole>IpsAdmin</defaultRole>
   <isValid>true</isValid>
</setUserInfoParam>
```

**응답**

없음.
