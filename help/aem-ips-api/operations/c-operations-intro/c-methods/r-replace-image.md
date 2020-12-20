---
description: 이미지 자산에 대한 이미지 데이터를 대체합니다.
seo-description: 이미지 자산에 대한 이미지 데이터를 대체합니다.
seo-title: replaceImage
solution: Experience Manager
title: replaceImage
topic: Scene7 Image Production System API
uuid: 46824e33-265c-4425-9ab1-8ad6b7ac154d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 15%

---


# replaceImage{#replaceimage}

이미지 자산에 대한 이미지 데이터를 대체합니다.

구문

## 인증된 사용자 유형 {#section-e2aad71fb2a54612badc7b16f82ed544}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-0d0ab668fa6d4310a93fb7ef8d8dd1e0}

**입력(replaceImageParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`companyName`*` | `xsd:string` | 예 | 교체할 이미지가 포함된 회사 핸들입니다. |
| ` *`assetHandle`*` | `xsd:string` | 예 | 바꾸려는 자산의 핸들입니다. |
| ` *`urlModifier`*` | `xsd:string` | 예 | 새 이미지 데이터를 생성하는 이미지 서버 명령. |

**출력(replaceImageReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | 예 | 새 에셋을 처리합니다. |

## 예제 {#section-cebb93576bde4cb98cb27356ca66783b}

이 코드 샘플은 이미지를 대신하고 `urlModifier`을(를) 교체 시 이미지 서버가 작업을 수행하지 않도록 지정하는 명령으로 적용합니다.

**요청**

```java
<replaceImageParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetHandle>a|140626|1|102524</assetHandle>
   <urlModifier>action=none</urlModifier>
</replaceImageParam>
```

**응답**

```java
<replaceImageReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|140626|1|102524</assetHandle>
</replaceImageReturn>
```

