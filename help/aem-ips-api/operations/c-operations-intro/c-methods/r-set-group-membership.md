---
description: 사용자의 그룹 구성원을 설정합니다.
solution: Experience Manager
title: setGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 0a355a34-1c2d-48c1-ba12-7d07d1673d09
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 12%

---

# setGroupMembership{#setgroupmembership}

사용자의 그룹 구성원을 설정합니다.

구문

## 인증된 사용자 유형 {#section-3d6308a8a5694ed085e04d1c37982b9e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-6aeda13b26af4796aad1306ac7a9ad17}

**입력(setGroupMembershipParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | 아니요 | 그룹 구성원을 설정하려는 사용자에 대한 핸들입니다. |
| `*`companyHandle`*` | `xsd:string` | 아니요 | 회사 핸들. |
| `*`groupHandleArray`*` | `types:HandleArray` | 예 | 사용자가 속한 그룹의 핸들 배열입니다. |

**출력(setGroupMembershipReturn)**

IPS API가 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-67b86d259df24938896fe19061845811}

이 코드 샘플은 사용자를 그룹의 구성원으로 만듭니다. 그룹 핸들 배열을 사용하여 여러 그룹에 사용자를 추가합니다.

**요청**

```java
<ns1:setGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>70|kmagnusson@adobe.com</ns1:userHandle>
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray>
      <ns1:items>225</ns1:items>
   </ns1:groupHandleArray>
</ns1:setGroupMembershipParam>
```

**응답**

없음.
