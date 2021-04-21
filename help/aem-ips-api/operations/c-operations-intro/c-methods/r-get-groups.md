---
description: 회사 그룹을 반환합니다.
solution: Experience Manager
title: getGroups
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 20%

---


# getGroups{#getgroups}

회사 그룹을 반환합니다.

구문

## 인증된 사용자 유형 {#section-27c77680a2f34e2f9ecd0af4ebb6847e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-0e06195f23dd4c69922df210f566dd18}

**입력(getGroupsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 회사의 손잡이입니다. |

**출력(getGroupsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`groupArray`*` | `types:GroupArray` | 예 | 그룹 배열입니다. |

## 예제 {#section-ed0708f611574354bf0c6ea83912b531}

이 코드는 특정 회사에 속하는 모든 그룹과 각 그룹에 대한 특정 정보를 포함하는 배열을 반환합니다.

**요청**

```java
<ns1:getGroupsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getGroupsParam>
```

```java
<getGroupsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupArray>
      <items>
         <groupHandle>225</groupHandle>
         <companyHandle>47</companyHandle>
         <name>MyGroup</name>
         <isSystemDefined>false</isSystemDefined>
      </items>
   </groupArray>
</getGroupsReturn>
```

