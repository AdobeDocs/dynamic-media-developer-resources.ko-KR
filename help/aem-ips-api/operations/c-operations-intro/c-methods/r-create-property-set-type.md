---
description: 속성 세트 유형은 속성 세트를 관리하는 데 사용되는 다양한 설정을 지정합니다.
solution: Experience Manager
title: createPropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 1730ccbf-e8b0-4f92-9daf-da2fa047cbbd
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 11%

---

# createPropertySetType{#createpropertysettype}

속성 세트 유형은 속성 세트를 관리하는 데 사용되는 다양한 설정을 지정합니다.

구문

## 인증된 사용자 유형 {#section-48e5f908276c4a549fd33a8828bad326}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-43dece72eb9f44df80f4a119dd2c008b}

**입력(createPropertySetTypeParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 아니요 | 속성 집합 유형을 소유한 회사의 핸들입니다. `companyHandle`이 전달되지 않고 호출자가 `IpsAdmin`이면 전역 속성 세트 유형이 만들어집니다. |
| `*`name`*` | `xsd:string` | 예 | 속성 세트 유형의 이름입니다. |
| `*`propertyType`*` | `xsd:string` | 예 | 속성 세트 유형을 선택합니다. |
| `*`allowMultiple`*` | `xsd:boolean` | 예 | 프로그램에 여러 속성 세트가 있을 수 있는지 확인합니다. |

**출력(createPropertySetTypeReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`typeHandle`*` | `xsd:string` | 예 | 유형의 핸들입니다. |

## 예제 {#section-13396c9639a6475190e622eae3cdb534}

이 코드 샘플은 `PropertySet Types` 상수로 지정된 이름과 형식으로 속성 세트를 만듭니다. 속성 집합 유형을 소유한 회사의 핸들입니다. companyHandle이 전달되지 않고 호출자가 IpsAdmin인 경우 전역 속성 집합 유형이 만들어집니다.

**요청**

```java
<createPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10803</typeHandle>
</createPropertySetTypeReturn>
```

**응답**

```java
<createPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</createPropertySetTypeReturn>
```
