---
description: 자산에 대한 게시 내역을 반환합니다.
solution: Experience Manager
title: getAssetPublishHistory
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f337e7f9-1af6-4164-b9bd-e697548e2850
TQID: 'https://experienceleague.adobe.com/fXYa2SsttVpR9a1bebJ1oouyK8peSZ5GdgldPqU9s1g'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 89
ht-degree: 15%

---

# getAssetPublishHistory{#getassetpublishhistory}

자산에 대한 게시 내역을 반환합니다.

구문

## 승인된 사용자 유형 {#section-3b9d6a129093458fa8890139a2718912}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-3541bd9914a44b89acfc1d419b560ee6}

**입력(getAssetPublishHistoryParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 자산 게시 기록이 있는 회사에 대한 핸들입니다. |
| assetHandle | `xsd:string` | 예 | 검사할 게시 기록이 있는 에셋입니다. |

**출력(getAssetPublishHistoryReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| pubHistoryArray | `types:PublishHistoryArray` | 예 | 에셋의 게시 내역. |

## 예제 {#section-53897c51e5a047c5bd5ea5a6efb2d114}

이 코드 샘플은 자산의 게시 내역을 반환합니다. 서버가 빈 배열을 반환하는 경우 자산이 게시된 적이 없습니다.

**요청**

```java
<getAssetPublishHistoryParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|732|1|535</assetHandle>
</getAssetPublishHistoryParam>
```

**응답**

```java
<getAssetPublishHistoryReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <pubHistoryArray/>
</getAssetPublishHistoryReturn>
```

