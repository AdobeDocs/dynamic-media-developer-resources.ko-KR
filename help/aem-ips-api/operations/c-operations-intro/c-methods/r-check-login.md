---
description: 특정 회사(ID로 식별), 이메일 주소 및 암호를 가진 사용자가 로그인할 수 있는지 확인합니다.
seo-description: 특정 회사(ID로 식별), 이메일 주소 및 암호를 가진 사용자가 로그인할 수 있는지 확인합니다.
seo-title: checkLogin
solution: Experience Manager
title: checkLogin
topic: Scene7 Image Production System API
uuid: 69f9e5f6-50c2-403d-93b2-b84a01f512a9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# checkLogin{#checklogin}

특정 회사(ID로 식별), 이메일 주소 및 암호를 가진 사용자가 로그인할 수 있는지 확인합니다.

>[!NOTE]
>
>회사 핸들이 생략된 경우 이 방법은 기본 사용자의 로그인을 확인합니다.

## 인증된 사용자 유형 {#section-df8b26b550854f899948276adaca083a}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-1ad4c0b4803b4388aedd655030676cb3}

**입력(checkLoginParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 아니요 | 사용자가 포함된 회사의 핸들 |
| ` *`이메일`*` | `xsd:string` | 예 | 사용자의 이메일 주소입니다. |
| ` *`암호`*` | `xsd:string` | 예 | 사용자의 암호입니다. |

**출력(checkLoginParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`status`*` | `xsd:string` | 예 | 사용자의 로그인 상태입니다. |

## 예제 {#section-23f90100a9d94bc7b4045634cccd1b98}

이 샘플 코드는 회사 핸들 매개 변수, 이메일 주소 및 암호를 사용하여 사용자가 IPS에 로그인할 수 있는지 여부를 결정합니다. 사용자가 로그인할 *수* 있으면 이 메서드는 문자열, 을 반환합니다 `ValidLogin`. 사용자가 로그인할 *수* 없으면 이 메서드는 문자열, 을 반환합니다 `InvalidLogin`.

**요청**

```java
<ns1:checkLoginParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>137</ns1:companyHandle>
   <ns1:email>juser3@scene7.com</ns1:email>
   <ns1:password>welcome</ns1:password>
</ns1:checkLoginParam>
```

**응답**

```java
<ns1:checkLoginReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:status>InvalidLogin</ns1:status>
</ns1:checkLoginReturn>
```

