---
description: 속성 세트와 연결된 모든 속성을 삭제합니다.
solution: Experience Manager
title: deletePropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 72429030-200d-4e13-a537-10a728998a26
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 13%

---

# deletePropertySet{#deletepropertyset}

속성 세트와 연결된 모든 속성을 삭제합니다.

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
| setHandle | `xsd:string` | 예 | 삭제할 속성 집합의 핸들입니다. |

**출력(deletePropertySetParam)**

IPS API가 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-cf319fc8f86a40ab9cbd838b031973fe}

이 코드 샘플은 집합의 핸들을 `deletePropertySetParam` 속성 집합을 삭제하기 위해 IPS 웹 서비스 서버로 전송됩니다.

**요청**

```java
<deletePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</deletePropertySetParam>
```

**응답**

없음.
