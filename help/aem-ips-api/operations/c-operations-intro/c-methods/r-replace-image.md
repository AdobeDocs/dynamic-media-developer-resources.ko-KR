---
description: 이미지 자산에 대한 이미지 데이터를 대체합니다.
solution: Experience Manager
title: replaceImage
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: bf8c1f5c-7829-4750-b5b7-b8b20d115d17
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 16%

---

# replaceImage{#replaceimage}

이미지 자산에 대한 이미지 데이터를 대체합니다.

구문

## 승인된 사용자 유형 {#section-e2aad71fb2a54612badc7b16f82ed544}

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
| companyName | `xsd:string` | 예 | 교체하려는 이미지가 있는 회사의 핸들입니다. |
| assetHandle | `xsd:string` | 예 | 바꿀 자산의 핸들입니다. |
| urlModifier | `xsd:string` | 예 | 새 이미지 데이터를 생성하는 이미지 서버 명령입니다. |

**출력(replaceImageReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| assetHandle | `xsd:string` | 예 | 새 자산을 처리합니다. |

## 예제 {#section-cebb93576bde4cb98cb27356ca66783b}

이 코드 샘플은 이미지를 대체하고 `urlModifier` 이미지 서버에서 교체 작업을 수행하지 않도록 지정하는 명령을 사용합니다.

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
