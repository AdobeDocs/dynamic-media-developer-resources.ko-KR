---
description: 그룹을 만들거나 편집합니다.
solution: Experience Manager
title: saveGroup
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1dd980e7-eb38-4c90-b4fc-83327d4a95f5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 20%

---

# saveGroup{#savegroup}

그룹을 만들거나 편집합니다.

구문

## 승인된 사용자 유형 {#section-a6c1ce4c69f44ad0bcd41bbf3893bc45}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-743610e98dd5494baffcbad6401038eb}

**입력(saveGroupParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 저장할 그룹이 있는 회사의 핸들입니다. |
| group핸들 | `xsd:string` | 아니요 | 그룹에 대한 핸들입니다. |
| name | `xsd:string` | 예 | 그룹 이름. |
| isSystemDefinition | `xsd:boolean` | 예 | `false` 는 기본값입니다. |

**출력(saveGroupReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| group핸들 | `xsd:string` | 예 | 그룹 핸들. |

## 예제 {#section-26eee227ff1f4edabb7fa1240b4d9999}

이 코드 샘플은 특정 회사에 속하는 그룹을 만듭니다. 그룹이 이미 있으면 지정한 매개변수 값과 함께 저장됩니다.

**요청**

```java
<ns1:saveGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:name>My Other Group</ns1:name>
   <ns1:isSystemDefined>false</ns1:isSystemDefined>
</ns1:saveGroupParam>
```

**응답**

```java
<saveGroupReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupHandle>281</groupHandle>
</saveGroupReturn>
```
