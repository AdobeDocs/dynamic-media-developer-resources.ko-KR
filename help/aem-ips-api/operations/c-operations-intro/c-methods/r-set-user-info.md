---
description: '사용자 속성(예: 이름, 이메일, 역할 등)을 설정합니다.'
seo-description: '사용자 속성(예: 이름, 이메일, 역할 등)을 설정합니다.'
seo-title: setUserInfo
solution: Experience Manager
title: setUserInfo
topic: Scene7 Image Production System API
uuid: 52e3a21e-1dd5-4f9d-b460-506d280fff47
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setUserInfo{#setuserinfo}

사용자 속성(예: 이름, 이메일, 역할 등)을 설정합니다.

구문

## 인증된 사용자 유형 {#section-6c28db5d15b3449492a73749e4f981ac}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-71b457921fe74acb862a1e112e550211}

**입력(setUserInfoParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:string` | 아니요 | 사용자 핸들 |
| ` *`firstName`*` | `xsd:string` | 예 | 이름. |
| ` *`lastName`*` | `xsd:string` | 예 | 성. |
| ` *`이메일`*` | `xsd:string` | 예 | 사용자 이메일. |
| ` *`defaultRole`*` | `xsd:string` | 예 | 사용자가 속한 각 회사의 사용자에 대한 역할을 설정합니다. 그러나 이 `IpsAdmin` 역할은 회사별 다른 설정을 무시합니다. |
| ` *`passwordExpires`*` | `xsd:dateTime` | 아니요 | 암호 만료 날짜를 설정합니다. |
| ` *`isValid`*` | `xsd:boolean` | 예 | 사용자가 유효한 IPS 사용자인지 확인합니다. |
| ` *`membershipArray`*` | `types:CompanyMembershipUpdateArray` | 예 | 회사 핸들의 배열입니다. |

**출력(set 파섹**

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
