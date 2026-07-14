---
description: 자산 이름을 회사의 이미지 제공/이미지 렌더링 카탈로그 네임스페이스의 모든 이름과 비교하여 IPS ID 충돌을 확인합니다.
solution: Experience Manager
title: checkAssetNames
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0756c4fc-64ec-4022-a6aa-fcf1542b41b0
TQID: 'https://experienceleague.adobe.com/RbFXhRqcaGXLMAeJhXMzho-ylSe2ktcKwvdbFtrcppM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 11%

---

# checkAssetNames{#checkassetnames}

자산 이름을 회사의 이미지 제공/이미지 렌더링 카탈로그 네임스페이스의 모든 이름과 비교하여 IPS ID 충돌을 확인합니다.

구문

## 승인된 사용자 유형 {#section-8efcbb3f555f417a870219e4714374db}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`
* `TrialSiteAdmin`
* `TrialSiteUser`

## 매개 변수 {#section-9c75b00f2072453abea0bdefc6ad7c99}

**입력(checkAssetNamesParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 아니요 | 사용자가 포함된 회사에 대한 핸들입니다. |
| assetNameArray | `types:StringArray` | 예 | 확인할 자산 이름의 배열입니다. |

**출력(checkAssetNamesReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| inUseNameArray | `types:StringArray` | 예 | 사용 중인 자산 이름의 배열입니다. |

## 예제 {#section-bc5d120d74614a63a425ca3acc337219}

이 샘플 코드는 지정된 회사에 대해 사용 중인 자산 이름을 요청합니다. 응답은 사용 중인 자산 이름 배열을 반환합니다.

**요청**

```java
<checkAssetNamesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <companyHandle>c|1</companyHandle>
   <assetNameArray>
      <items>ABC123</items>
      <items>DEF456</items>
   </assetNameArray>
</checkAssetNamesParam>
```

**응답**

```java
<checkAssetNamesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <inUseNameArray>
      <items>DEF456</items>
   </inUseNameArray>
</checkAssetNamesReturn>
```

