---
description: 특정 회사 및 그룹에 속하는 사용자를 가져옵니다.
solution: Experience Manager
title: getGroupMembers
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 17%

---


# getGroupMembers{#getgroupmembers}

특정 회사 및 그룹에 속하는 사용자를 가져옵니다.

구문

## 인증된 사용자 유형 {#section-08a73460d122480292205bb8f2df9220}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-b798b06354c946abbb90fa72cc9c67fd}

**입력(getGroupMembersParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 회사의 손잡이입니다. |
| `*`groupHandle`*` | `xsd:string` |  | 그룹의 핸들입니다. |

**출력(getGroupMembersReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`userHandleArray`*` | `type:HandleArray` | 예 | 사용자 핸들의 배열입니다. |

## 예제 {#section-aaa340dba6b64cce9bcd8303cf999166}

이 코드 샘플은 특정 그룹에 속한 모든 사용자가 포함된 사용자 핸들 배열을 반환합니다.

**요청**

```java
<ns1:getGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
</ns1:getGroupMembersParam>
```

**응답**

```java
<getGroupMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userHandleArray>
      <items>70|kmagnusson@adobe.com</items>
   </userHandleArray>
</getGroupMembersReturn>
```

