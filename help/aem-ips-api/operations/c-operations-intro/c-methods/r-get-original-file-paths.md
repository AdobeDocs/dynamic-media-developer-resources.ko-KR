---
description: 회사 자산의 원본 파일 경로를 가져옵니다.
solution: Experience Manager
title: getOriginalFilePaths
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81d06a8c-55c1-47d5-adc9-928ab30199c6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 16%

---

# getOriginalFilePaths{#getoriginalfilepaths}

회사 자산의 원본 파일 경로를 가져옵니다.

구문

## 승인된 사용자 유형 {#section-da8d8561e9174e938f3595a5d6e50089}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>에셋에 대한 읽기 액세스 권한이 필요합니다.

## 매개 변수 {#section-a6b394daba6e49a8882cf3051035d9d1}

**입력(getOriginalFilePathsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 회사 손잡이. |
| assetHandleArray | `types:HandleArray` | 예 | 원래 파일 경로를 가져오려는 자산에 대한 핸들 배열입니다. |

**출력(getOriginalFilePathsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| originalFileArray | `types:StringArray` | 예 | 원래 파일 경로를 나타내는 문자열 배열입니다. |

## 예제 {#section-a966e783a2ba49f5b6b0f961329ab2f8}

이 코드 샘플은 에셋 핸들 배열에 고유한 에셋 핸들로 지정된 에셋의 파일 경로를 반환합니다.

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
