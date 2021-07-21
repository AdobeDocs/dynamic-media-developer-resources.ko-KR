---
description: 이미지 세트를 업데이트합니다.
solution: Experience Manager
title: updateImageSet
feature: Dynamic Media Classic,SDK/API,이미지 세트
role: Developer,Admin
exl-id: d8d5fb80-17f1-424f-8a61-27189f87d603
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 18%

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
| `*`memberArray`*` | `types:ImageSetMemberUpdateArray` | 아니요 | 이미지 세트 멤버를 재설정합니다. |
| `*`thumbAssetHandle`*` | `xsd:string` | 아니요 | 이미지 세트의 축소판 역할을 하는 자산의 핸들입니다. |

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
