---
description: 회사 자산의 원본 파일 경로를 가져옵니다.
seo-description: 회사 자산의 원본 파일 경로를 가져옵니다.
seo-title: getOriginalFilePaths
solution: Experience Manager
title: getOriginalFilePaths
topic: Dynamic Media Image Production System API
uuid: c4acf288-1a57-4295-806b-348f15a089cc
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 14%

---


# getOriginalFilePaths{#getoriginalfilepaths}

회사 자산의 원본 파일 경로를 가져옵니다.

구문

## 인증된 사용자 유형 {#section-da8d8561e9174e938f3595a5d6e50089}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>자산에 대한 읽기 액세스 권한이 필요합니다.

## 매개 변수 {#section-a6b394daba6e49a8882cf3051035d9d1}

**입력(getOriginalFilePathsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 회사의 손잡이입니다. |
| `*`assetHandleArray`*` | `types:HandleArray` | 예 | 가져오려는 원본 파일 경로를 가진 자산의 핸들 배열입니다. |

**출력(getOriginalFilePathsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`originalFileArray`*` | `types:StringArray` | 예 | 원본 파일 경로를 나타내는 문자열 배열입니다. |

## 예제 {#section-a966e783a2ba49f5b6b0f961329ab2f8}

이 코드 샘플은 자산 핸들 배열에서 고유한 자산 핸들을 사용하여 지정된 자산의 파일 경로를 반환합니다.

**요청**

```java
<ns1:getOriginalFilePathsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandleArray>
      <ns1:items>24265|1|17061</ns1:items>
      <ns1:items>24267|1|17063</ns1:items>
   </ns1:assetHandleArray>
</ns1:getOriginalFilePathsParam>
```

**응답**

```java
<getOriginalFilePathsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <originalFileArray>
      <items>MyCompany/Autumn Leaves.jpg</items>
      <items>MyCompany/Desert Landscape.jpg</items>
   </originalFileArray>
</getOriginalFilePathsReturn>
```

