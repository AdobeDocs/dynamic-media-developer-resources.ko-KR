---
description: 자산을 특정 폴더로 이동합니다.
solution: Experience Manager
title: moveAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c5357c1a-92ac-4f9c-957e-b62cb812796c
TQID: 'https://experienceleague.adobe.com/-3pTSenps7g41lho728JLME6EwS2xlYLBfJnuAF6DXY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 14%

---

# moveAsset{#moveasset}

자산을 특정 폴더로 이동합니다.

구문

## 승인된 사용자 유형 {#section-e4f2d2a58132450aa36da6377134211e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-dd0bbdf293aa4563af70a91f97c861f1}

**입력(moveAssetParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 회사를 위해 처리하십시오. |
| assetHandle | `xsd:string` | 예 | 이동할 자산을 처리합니다. |
| folder핸들 | `xsd:string` | 예 | 대상 폴더에 대한 를 처리합니다. |

**출력(moveAssetReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-78333769f4f14e2886fdf06433c9d2ad}

이 코드 샘플은 자산을 폴더로 이동합니다.

**요청**

```java
<ns1:moveAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24266|1|17062</ns1:assetHandle>
   <ns1:folderHandle>MyCompany/My New Images/</ns1:folderHandle>
</ns1:moveAssetParam>
```

**응답**

없음.

