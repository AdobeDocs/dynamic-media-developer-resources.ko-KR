---
description: 새 암호를 생성합니다.
solution: Experience Manager
title: generatePassword
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 80e7642f-4aec-4ff0-a090-e59b7a065c39
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 20%

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
| 암호 | `xsd:string` | 예 | 새 암호입니다. |

## 예제 {#section-f580fefdccec46fe95359e3aef0ed17f}

이 코드 샘플은 암호를 생성합니다. 요청이 둘러싸인 요소나 값이 없는 매개 변수이므로 이는 이례적인 일입니다. IPS는 강력한 암호를 반환합니다.

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
