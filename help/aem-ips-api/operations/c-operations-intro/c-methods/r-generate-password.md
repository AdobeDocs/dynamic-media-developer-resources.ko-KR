---
description: 새 암호를 생성합니다.
seo-description: 새 암호를 생성합니다.
seo-title: generatePassword
solution: Experience Manager
title: generatePassword
uuid: e3367bfc-d437-4a61-83e8-69830154dc61
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 16%

---


# generatePassword{#generatepassword}

새 암호를 생성합니다.

구문

## 인증된 사용자 유형 {#section-88f7dc11e5c74be281399d8f2e3c9555}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-d516615c906240819a284786efb19863}

**입력(generatePasswordParam)**

없음.

**출력(generatePasswordParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`암호`*` | `xsd:string` | 예 | 새 암호입니다. |

## 예제 {#section-f580fefdccec46fe95359e3aef0ed17f}

이 코드 샘플은 암호를 생성합니다. 요청이 포함된 요소나 값이 없는 매개 변수일 뿐이므로 이는 예외입니다. IPS는 강력한 암호를 반환합니다.

**요청**

```java
<generatePasswordParam xmlns="http://www.scene7.com/IpsApi/xsd">
</generatePasswordParam>
```

**응답**

```java
<generatePasswordReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <password>1\7aQRn]</password>
</generatePasswordReturn>
```

