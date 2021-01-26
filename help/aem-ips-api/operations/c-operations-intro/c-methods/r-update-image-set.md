---
description: 이미지 세트를 업데이트합니다.
seo-description: 이미지 세트를 업데이트합니다.
seo-title: updateImageSet
solution: Experience Manager
title: updateImageSet
topic: Dynamic Media Image Production System API
uuid: df118ba3-d86f-4005-928e-76a5a9f899fc
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 19%

---


# updateImageSet{#updateimageset}

이미지 세트를 업데이트합니다.

구문

## 매개 변수 {#section-3be47dbbce474ce78676b05e163492e3}

**입력(updateImageSetParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 수정할 이미지 세트가 포함된 회사의 핸들입니다. |
| `*`assetHandle`*` | `xsd:string` | 예 | 수정할 이미지 세트의 핸들입니다. |
| `*`memberArray`*` | `types:ImageSetMemberUpdateArray` | 아니요 | 이미지 집합 구성원을 재설정합니다. |
| `*`thumbAssetHandle`*` | `xsd:string` | 아니요 | 이미지 세트의 축소판으로 사용되는 자산의 핸들입니다. |

**출력(updateImageSetReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`시퀀스`*` |  |  |  |

## 예제 {#section-ce47a4b6e062423fa55ed3a0fd26d7ff}

**요청**

```java
<updateImageSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <companyHandle>c|15</companyHandle> 
  <assetHandle>a|381</assetHandle> 
  <memberArray> 
    <items> 
      <assetHandle>a|374</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
    <items> 
      <assetHandle>a|375</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
    <items> 
      <assetHandle>a|376</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
  </memberArray> 
  <thumbAssetHandle>a|376</thumbAssetHandle> 
</updateImageSetParam>
```

**응답**

```java
<updateImageSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"/>
```

