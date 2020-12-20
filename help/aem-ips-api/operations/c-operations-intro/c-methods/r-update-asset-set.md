---
description: 자산 세트를 업데이트합니다.
seo-description: 자산 세트를 업데이트합니다.
seo-title: updateAssetSet
solution: Experience Manager
title: updateAssetSet
topic: Scene7 Image Production System API
uuid: e844a395-0ab3-45a7-bcec-8e9e15efc70e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 20%

---


# updateAssetSet{#updateassetset}

자산 세트를 업데이트합니다.

구문

## 매개 변수 {#section-d7080ccd97334c94860eb107a3e132b2}

**입력(updateAssetSetParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 예 | 수정할 이미지 세트가 포함된 회사의 핸들입니다. |
| ` *`assetHandle`*` | `xsd:string` | 예 | 수정할 이미지 세트의 핸들입니다. |
| ` *`setDefinition`*` | `xsd:string` | 아니요 | 이미지 집합 구성원을 재설정합니다. |
| ` *`thumbAssetHandle`*` | `xsd:string` | 아니요 | 이미지 세트의 축소판으로 사용되는 자산의 핸들입니다. |

**출력(updateAssetSetReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
|  |  |  |  |

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

