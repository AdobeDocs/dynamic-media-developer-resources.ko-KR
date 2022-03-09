---
description: 자산을 특정 폴더로 이동합니다.
solution: Experience Manager
title: moveAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c5357c1a-92ac-4f9c-957e-b62cb812796c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 17%

---

# moveAsset{#moveasset}

자산을 특정 폴더로 이동합니다.

구문

## 인증된 사용자 유형 {#section-e4f2d2a58132450aa36da6377134211e}

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
| companyHandle | `xsd:string` | 예 | 회사를 담당합니다. |
| assetHandle | `xsd:string` | 예 | 이동할 자산을 처리합니다. |
| folderHandle | `xsd:string` | 예 | 대상 폴더로 처리합니다. |

**출력(moveAssetReturn)**

IPS API가 이 작업에 대한 응답을 반환하지 않습니다.

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
