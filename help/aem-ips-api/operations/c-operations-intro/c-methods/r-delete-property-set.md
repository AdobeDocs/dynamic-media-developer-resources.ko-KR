---
description: 속성 세트와 모든 관련 속성을 삭제합니다.
seo-description: 속성 세트와 모든 관련 속성을 삭제합니다.
seo-title: deletePropertySet
solution: Experience Manager
title: deletePropertySet
topic: Scene7 Image Production System API
uuid: b4fdf51f-89ec-4a69-9179-078ee8e1937f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`setHandle`*` | `xsd:string` | 예 | 삭제할 속성 집합에 대한 핸들입니다. |

**출력(deletePropertySetParam)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-cf319fc8f86a40ab9cbd838b031973fe}

이 코드 샘플에서는 IPS 웹 서비스 서버로 `deletePropertySetParam` 보낸 세트의 핸들을 필드로 사용하여 속성 집합을 삭제합니다.

**요청**

```java
<deletePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</deletePropertySetParam>
```

**응답**

없음.
