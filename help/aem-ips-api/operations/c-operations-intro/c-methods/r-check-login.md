---
description: 특정 회사(핸들로 식별됨), 이메일 주소 및 암호를 가진 사용자가 로그인할 수 있는지 확인합니다.
solution: Experience Manager
title: checkLogin
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 1f96f376-574c-464b-9c89-c215f6454b81
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 12%

---

# checkLogin{#checklogin}

특정 회사(핸들로 식별됨), 이메일 주소 및 암호를 가진 사용자가 로그인할 수 있는지 확인합니다.

>[!NOTE]
>
>회사 핸들을 생략하면 이 메서드는 기본 사용자의 로그인을 확인합니다.

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
| `*`companyHandle`*` | `xsd:string` | 아니요 | 사용자가 포함된 회사의 핸들입니다. |
| `*`이메일`*` | `xsd:string` | 예 | 사용자의 이메일 주소입니다. |
| `*`암호`*` | `xsd:string` | 예 | 사용자의 암호입니다. |

**출력(checkLoginParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`status`*` | `xsd:string` | 예 | 사용자의 로그인 상태입니다. |

## 예제 {#section-23f90100a9d94bc7b4045634cccd1b98}

이 샘플 코드는 회사 핸들 매개 변수, 전자 메일 주소 및 암호를 사용하여 사용자가 IPS에 로그인할 수 있는지 여부를 결정합니다. 사용자 *이(가)*&#x200B;로그인할 수 있으면 이 메서드는 문자열 `ValidLogin`를 반환합니다. 사용자 *이(가)*&#x200B;로그인할 수 없는 경우 이 메서드는 문자열 `InvalidLogin`를 반환합니다.

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
