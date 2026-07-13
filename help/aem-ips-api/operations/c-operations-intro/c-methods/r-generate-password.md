---
description: 새 암호를 생성합니다.
solution: Experience Manager
title: generatePassword
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 80e7642f-4aec-4ff0-a090-e59b7a065c39
TQID: 'https://experienceleague.adobe.com/3XFwGq8wAf81wEUfaUrcDiI03MNe0bhMCBdV-5LDfoQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 59
ht-degree: 16%

---

# generatePassword{#generatepassword}

새 암호를 생성합니다.

구문

## 승인된 사용자 유형 {#section-88f7dc11e5c74be281399d8f2e3c9555}

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
| 암호 | `xsd:string` | 예 | 새 암호. |

## 예제 {#section-f580fefdccec46fe95359e3aef0ed17f}

이 코드 샘플은 암호를 생성합니다. 요청은 둘러싸인 요소나 값이 없는 매개 변수일 뿐이므로 이례적입니다. IPS는 강력한 암호를 반환합니다.

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

