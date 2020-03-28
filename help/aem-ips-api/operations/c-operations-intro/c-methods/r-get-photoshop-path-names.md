---
description: 지정된 이미지에 대한 Photoshop 경로 이름의 배열을 반환합니다.
seo-description: 지정된 이미지에 대한 Photoshop 경로 이름의 배열을 반환합니다.
seo-title: getPhotoshopPathNames
solution: Experience Manager
title: getPhotoshopPathNames
topic: Scene7 Image Production System API
uuid: d3f1dea5-393b-498e-963d-37a4e38068a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getPhotoshopPathNames{#getphotoshoppathnames}

지정된 이미지에 대한 Photoshop 경로 이름의 배열을 반환합니다.

구문

## 인증된 사용자 유형 {#section-baa0fd4b92bc4ad89809efd659b3a629}

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
| ` *`companyHandle`*` | `xsd:string` | 예 | 작업할 이미지가 포함된 회사를 처리합니다. |
| ` *`assetHandle`*` | `xsd:string` | 예 | 이미지 자산에 대한 핸들 |

**출력(getPhotoshopPathNamesReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`pathNameArray`*` | `types:StringArray` | 예 | 이미지의 Photoshop 경로 이름 배열입니다. |

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

