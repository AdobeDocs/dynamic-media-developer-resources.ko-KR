---
description: 이미지 집합에 포함된 멤버 배열을 가져옵니다.
seo-description: 이미지 집합에 포함된 멤버 배열을 가져옵니다.
seo-title: getImageSetMembers
solution: Experience Manager
title: getImageSetMembers
topic: Scene7 Image Production System API
uuid: b19c9fec-df92-42e1-9228-42cdf196fdfc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 15%

---


# getImageSetMembers{#getimagesetmembers}

이미지 집합에 포함된 멤버 배열을 가져옵니다.

구문

## 인증된 사용자 유형 {#section-eaa3a167fa77403ea1b374b05fff4ded}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>이미지 및 멤버 세트 자산에 대한 읽기 액세스 권한이 필요합니다.

## 매개 변수 {#section-a67ba98095574533980997c83ceaa316}

**입력(getImageSetMembersParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 예 | 이미지 세트가 포함된 회사의 핸들입니다. |
| ` *`assetHandle`*` | `xsd:string` | 예 | 이미지 집합 자산 핸들. |

**출력(getImageSetMembersReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`memberArray`*` | `types:ImageSetMemberArray` | 아니요 | 이미지 집합 멤버의 배열입니다. |

## 예제 {#section-888a9a78033346f39b171229de93dfa0}

이 코드 샘플은 특정 이미지 집합 멤버를 반환합니다. 응답에서 빈 배열을 반환합니다.

**요청**

```java
<ns1:getImageSetMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>34195|22|927</ns1:assetHandle>
</ns1:getImageSetMembersParam>
```

**응답**

```java
<getImageSetMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <memberArray></memberArray>
</getImageSetMembersReturn>
```

