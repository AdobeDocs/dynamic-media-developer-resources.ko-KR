---
description: 지정된 이미지에 대한 Photoshop 경로 이름의 배열을 반환합니다.
solution: Experience Manager
title: getPhotoshopPathNames
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 11d4c0d0-a3a3-4324-a4a6-1dd7b7e673da
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 20%

---

# getPhotoshopPathNames{#getphotoshoppathnames}

지정된 이미지에 대한 Photoshop 경로 이름의 배열을 반환합니다.

구문

## 승인된 사용자 유형 {#section-baa0fd4b92bc4ad89809efd659b3a629}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-605a4aab23104489a21f7f7f5849801b}

**입력(getPhotoshopPathNamesParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 작업할 이미지가 포함된 회사를 처리합니다. |
| assetHandle | `xsd:string` | 예 | 이미지 에셋에 대해 처리합니다. |

**출력(getPhotoshopPathNamesReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| pathNameArray | `types:StringArray` | 예 | 이미지에 있는 Photoshop 경로 이름의 배열입니다. |

## 예제 {#section-6d316f14b4184d42af4ca3f717b042dd}

**요청**

```java
<getPhotoshopPathNamesParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <companyHandle>c|301</companyHandle>
  <assetHandle>a|26014</assetHandle>
</getPhotoshopPathNamesParam>
```

**응답**

```java
<getPhotoshopPathNamesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <pathNameArray>
    <items>Background Path</items>
    <items>Face Path</items>
  </pathNameArray>
</getPhotoshopPathNamesReturn>
```
