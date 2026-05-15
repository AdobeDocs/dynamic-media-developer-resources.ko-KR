---
description: 이미지 자산에 대한 이미지 데이터를 대체합니다.
solution: Experience Manager
title: replaceImage
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: bf8c1f5c-7829-4750-b5b7-b8b20d115d17
TQID: 'https://experienceleague.adobe.com/11bWPLId2s4gOVhiIFr93Ca4D-7SJ0PYHFmiSKtStjk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 101
ht-degree: 14%

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

이 코드 샘플은 이미지를 바꾸고 이미지 서버가 대체 작업을 수행하지 않도록 지정하는 명령으로 `urlModifier`을(를) 적용합니다.

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
