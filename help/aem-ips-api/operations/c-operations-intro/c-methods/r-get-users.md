---
description: 회사, 그룹 및 사용자 역할 처리에서 지정한 사용자 배열을 가져옵니다. 이 작업을 사용하면 반환된 사용자를 정렬하고 문자별로 필터링할 수 있습니다.
solution: Experience Manager
title: getUsers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dfdcbcdd-232f-4c73-9520-c7c958eedf54
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 10%

---

# getUsers{#getusers}

회사, 그룹 및 사용자 역할 처리에서 지정한 사용자 배열을 가져옵니다. 이 작업을 사용하면 반환된 사용자를 정렬하고 문자별로 필터링할 수 있습니다.

## 인증된 사용자 유형 {#section-6a8f23cc6b22442d8776f701016971ed}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`


| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`inactive`*` | `xsd:boolean` | 아니요 | 비활성 사용자를 포함하거나 제외합니다. IPS가 아닌 관리자 사용자는 API 호출을 수행할 수 있는 권한이 있는 적어도 하나의 회사의 활성 구성원이어야 합니다. 사용자에게 활성 회사 멤버십이 없는 경우 인증 오류가 반환됩니다. |
| `*`includeInvalid`*` | `xsd:boolean` | 아니요 | 잘못된 사용자를 포함/제외할 수 있습니다. |
| `*`companyHandleArray`*` | `types:HandleArray` | 아니요 | 회사별로 결과를 필터링합니다. |
| `*`groupHandleArray`*` | `types:HandleArray` | 아니요 | 그룹별로 결과를 필터링합니다. |
| `*`userRoleArray`*` | `types:StringArray` | 아니요 | 사용자 역할별로 결과를 필터링합니다. |
| `*`charFilterField`*` | `xsd:string` | 아니요 | 필드의 문자열 접두사별로 결과를 필터링합니다(참조: [!DNL Trash State).] |
| `*`charFilter`*` | `xsd:string` | 아니요 | 특정 문자별로 결과를 필터링합니다. |
| `*`sortBy`*` | `xsd:string` | 아니요 | 사용자 정렬 필드 선택. |
| `*`recordsPerPage`*` | `xsd:int` | 아니요 | 페이지당 지정된 레코드 수를 반환합니다. |
| `*`resultsPage`*` | `xsd:int` | 아니요 | 결과 페이지. |

**출력(getUsersReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`userArray`*` | `types:UserArray` | 예 | 사용자 배열입니다. |

## 예제 {#section-bc43a5dd7b4c4f048d25fc881554dab2}

이 코드 샘플은 몇 가지 선택적 매개 변수에 대한 사용자 배열을 반환합니다. 사용자 역할, 사용자 문자 필터 필드 및 사용자 정렬 필드는 특정 문자열 상수를 사용하여 결정됩니다.

**요청**

```java
<ns1:getUsersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:includeInvalid>false</ns1:includeInvalid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
   <ns1:userRoleArray>
      <ns1:items>IpsAdmin</ns1:items>
   </ns1:userRoleArray>
   <ns1:sortBy>LastName</ns1:sortBy>
</ns1:getUsersParam>
```

**응답**

```java
<getUsersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userArray>
      <items>
         <userHandle>70|kmagnusson@adobe.com</userHandle>
         <firstName>Kris</firstName>
         <lastName>Magnusson</lastName>
         <email>kmagnusson@adobe.com</email>
         <role>IpsAdmin</role>
         <isValid>true</isValid>
         <passwordExpires>2107-07-27T15:18:15.816-07:00</passwordExpires>
      </items>
      ...
   </userArray>
</getUsersReturn>
```
