---
description: 자산 세트를 업데이트합니다.
solution: Experience Manager
title: updateAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: af7899c4-a95f-42c8-858e-ed1592c6f5b6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 19%

---

# updateAsset{#updateassetset}

자산 세트를 업데이트합니다.

구문

## 매개 변수 {#section-d7080ccd97334c94860eb107a3e132b2}

**입력(updateAssetSetParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 수정할 이미지 세트가 포함된 회사에 대한 핸들입니다. |
| assetHandle | `xsd:string` | 예 | 수정할 이미지 세트에 대한 핸들입니다. |
| setDefinition | `xsd:string` | 아니요 | 이미지 집합 구성원을 재설정합니다. |
| thumbAssetHandle | `xsd:string` | 아니요 | 이미지 세트의 썸네일 역할을 하는 에셋의 핸들입니다. |

**출력(updateAssetSetReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
|   |  |  |  |

## 예제 {#section-ce47a4b6e062423fa55ed3a0fd26d7ff}

**요청**

```java
<updateAssetSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <companyHandle>c|15</companyHandle> 
  <assetHandle>a|535</assetHandle> 
  <setDefinition>${getCatalogId([a|202])};${getCatalogId([a|202])};advanced_image;,${getCatalogId([a|935])};${getCatalogId([a|935])};advanced_image;,${getCatalogId([a|933])};${getCatalogId([a|933])};advanced_image;</setDefinition> 
  <thumbAssetHandle>a|202</thumbAssetHandle> 
</updateAssetSetParam>
```

**응답**

```java
<updateAssetSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"/>
```
