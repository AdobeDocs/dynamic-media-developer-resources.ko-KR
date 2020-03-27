---
description: 사용자에 대한 정보를 가져옵니다. 시스템 사용자의 이메일 주소와 암호를 요청 인증을 위한 자격 증명으로 사용하십시오. 그렇지 않으면 기본 사용자에 대한 정보를 가져옵니다.
seo-description: 사용자에 대한 정보를 가져옵니다. 시스템 사용자의 이메일 주소와 암호를 요청 인증을 위한 자격 증명으로 사용하십시오. 그렇지 않으면 기본 사용자에 대한 정보를 가져옵니다.
seo-title: getUserInfo
solution: Experience Manager
title: getUserInfo
topic: Scene7 Image Production System API
uuid: b305c108-22e9-4268-a5b3-25fddd844c24
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getUserInfo{#getuserinfo}

사용자에 대한 정보를 가져옵니다. 시스템 사용자의 이메일 주소와 암호를 요청 인증을 위한 자격 증명으로 사용하십시오. 그렇지 않으면 기본 사용자에 대한 정보를 가져옵니다.

구문

## 인증된 사용자 유형 {#section-1c42d78e914a4b84a946b3480f29b36a}

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
| ` *`userHandle`*` | `xsd:string` | 아니요 | 정보를 반환할 사용자를 처리합니다. |
| ` *`이메일`*` | `xsd:string` | 아니요 | 사용자 이메일 주소입니다. |

**출력(getUserInfoReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`userInfo`*` | `types:User` | 예 | 사용자의 이름, 성, 이메일 주소 및 역할뿐만 아니라 사용자의 유효 여부 및 암호가 만료된 시기 |

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

