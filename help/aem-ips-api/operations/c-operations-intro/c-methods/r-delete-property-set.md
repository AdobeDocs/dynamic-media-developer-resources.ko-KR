---
description: 속성 세트와 모든 관련 속성을 삭제합니다.
solution: Experience Manager
title: deletePropertySet
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 12%

---


# deletePropertySet{#deletepropertyset}

속성 세트와 모든 관련 속성을 삭제합니다.

구문

## 인증된 사용자 유형 {#section-b54aa8c854de400a989b4957412ff42c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-e5fc868f69494cf6858e03027db09101}

**입력(deletePropertySetParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`setHandle`*` | `xsd:string` | 예 | 삭제할 속성 집합에 대한 핸들입니다. |

**출력(deletePropertySetParam)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-cf319fc8f86a40ab9cbd838b031973fe}

이 코드 샘플에서는 속성 집합을 삭제하기 위해 IPS 웹 서비스 서버로 보낸 `deletePropertySetParam`의 필드로 세트의 핸들을 사용합니다.

**요청**

```java
<deletePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</deletePropertySetParam>
```

**응답**

없음.
