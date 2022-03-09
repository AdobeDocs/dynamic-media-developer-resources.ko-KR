---
description: 속성 세트 유형과 관련 속성 집합 및 속성을 삭제합니다.
solution: Experience Manager
title: deletePropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 97ec0f41-794f-4340-b86d-ab07a742d447
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 11%

---

# deletePropertySetType{#deletepropertysettype}

속성 세트 유형과 관련 속성 집합 및 속성을 삭제합니다.

구문

## 인증된 사용자 유형 {#section-16a17b4ebf9a4639bdb2784a2e9fe00d}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-1c8973f5d35f44b4a6a483a41609e455}

**입력(deletePropertySetTypeParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| typeHandle | `xsd:string` | 예 | 삭제할 속성 집합 유형에 대한 핸들입니다. |

**출력(deletePropertySetTypeParam)**

IPS API가 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-85faa2e3411a4e23aa6489037f7ce078}

이 코드 샘플은 형식의 핸들을 `deletePropertySetTypeParam` 속성 세트 유형을 삭제하기 위해 IPS 웹 서비스 서버로 전송됩니다.

**요청**

```java
<deletePropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</deletePropertySetTypeParam>
```

**응답**

없음.
