---
description: 사용자에 대한 정보를 가져옵니다. 시스템 사용자의 이메일 주소와 암호를 요청 인증을 위한 자격 증명으로 사용합니다. 그렇지 않으면 기본 사용자에 대한 정보를 가져옵니다.
solution: Experience Manager
title: getUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1981f25f-779e-4434-ab6b-0debb40521fe
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 10%

---

# getUserInfo{#getuserinfo}

사용자에 대한 정보를 가져옵니다. 시스템 사용자의 이메일 주소와 암호를 요청 인증을 위한 자격 증명으로 사용합니다. 그렇지 않으면 기본 사용자에 대한 정보를 가져옵니다.

구문

## 승인된 사용자 유형 {#section-1c42d78e914a4b84a946b3480f29b36a}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-e87b3cb743494719925c9458eed433b6}

**입력(getUserInfoParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| 사용자 핸들 | `xsd:string` | 아니요 | 정보를 반환하려는 사용자에게 을 처리합니다. |
| 이메일 | `xsd:string` | 아니요 | 사용자 이메일 주소. |

**출력(getUserInfoReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| userInfo | `types:User` | 예 | 사용자의 이름, 성, 이메일 주소 및 역할과 사용자가 유효한지 여부 및 사용자 암호가 만료되는 시기. |

## 예제 {#section-98d77a2e360a438dbe240099bea26a65}

이 코드 샘플은 기본 IPS 사용자에 대한 정보를 반환합니다.

**요청**

```java
<getUserInfoParam xmlns="http://www.scene7.com/IpsApi/xsd" /></getUserInfoParam>
```

**응답**

```java
<ns1:getUserInfoReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd"> 
   <ns1:userInfo> 
      <ns1:userHandle>3261|user@scene7.com</ns1:userHandle> 
      <ns1:firstName>FirstName</ns1:firstName> 
      <ns1:lastName>LastName</ns1:lastName> 
      <ns1:email>user@scene7.com</ns1:email> 
      <ns1:role>IpsAdmin</ns1:role> 
      <ns1:isValid>true</ns1:isValid> 
      <ns1:passwordExpires>2107-04-22T18:35:41.995Z</ns1:passwordExpires> 
   </ns1:userInfo> 
</ns1:getUserInfoReturn>
```
