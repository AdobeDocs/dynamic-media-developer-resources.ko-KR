---
description: 회사, 그룹 및 사용자 역할 핸들에 의해 지정된 사용자 배열을 가져옵니다. 이 작업을 통해 반환된 사용자를 정렬하고 문자별로 필터링할 수 있습니다.
seo-description: 회사, 그룹 및 사용자 역할 핸들에 의해 지정된 사용자 배열을 가져옵니다. 이 작업을 통해 반환된 사용자를 정렬하고 문자별로 필터링할 수 있습니다.
seo-title: getUsers
solution: Experience Manager
title: getUsers
topic: Dynamic Media Image Production System API
uuid: f16ccd1b-0f00-4d9a-b6e1-6abc3bde1af9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 9%

---


# getUsers{#getusers}

회사, 그룹 및 사용자 역할 핸들에 의해 지정된 사용자 배열을 가져옵니다. 이 작업을 통해 반환된 사용자를 정렬하고 문자별로 필터링할 수 있습니다.

## 인증된 사용자 유형 {#section-6a8f23cc6b22442d8776f701016971ed}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`


| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`includeInactive`*` | `xsd:boolean` | 아니요 | 비활성 사용자 포함 또는 제외 IPS 관리자가 아닌 사용자는 API 호출을 수행할 수 있는 권한을 부여받을 수 있는 하나 이상의 회사의 활성 구성원이어야 합니다. 사용자에게 유효한 회사 멤버십이 없는 경우 인증 오류가 반환됩니다. |
| `*`includeInvalid`*` | `xsd:boolean` | 아니요 | 잘못된 사용자를 포함/제외할 수 있습니다. |
| `*`companyHandleArray`*` | `types:HandleArray` | 아니요 | 회사별로 결과를 필터링합니다. |
| `*`groupHandleArray`*` | `types:HandleArray` | 아니요 | 그룹별로 결과를 필터링합니다. |
| `*`userRoleArray`*` | `types:StringArray` | 아니요 | 사용자 역할별로 결과를 필터링합니다. |
| `*`charFilterField`*` | `xsd:string` | 아니요 | 필드의 문자열 접두사로 결과 필터링( [!DNL Trash State).] 참조) |
| `*`charFilter`*` | `xsd:string` | 아니요 | 특정 문자별로 결과를 필터링합니다. |
| `*`sortBy`*` | `xsd:string` | 아니요 | 사용자 정렬 필드 선택 |
| `*`recordsPerPage`*` | `xsd:int` | 아니요 | 페이지당 지정된 레코드 수를 반환합니다. |
| `*`resultsPage`*` | `xsd:int` | 아니요 | 결과 페이지를 참조하십시오. |

**출력(getUsersReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`userArray`*` | `types:UserArray` | 예 | 사용자 배열입니다. |

## 예제 {#section-bc43a5dd7b4c4f048d25fc881554dab2}

이 코드 샘플은 여러 선택적 매개 변수에 대한 사용자 배열을 반환합니다. 사용자 역할, 사용자 문자 필터 필드 및 사용자 정렬 필드는 특정 문자열 상수를 사용하여 결정됩니다.

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

