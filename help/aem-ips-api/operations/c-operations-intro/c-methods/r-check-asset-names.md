---
description: 자산 이름을 회사의 이미지 제공/이미지 렌더링 카탈로그 네임스페이스와 모든 이름과 비교하여 IPS ID 충돌을 확인합니다.
solution: Experience Manager
title: checkAssetNames
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0756c4fc-64ec-4022-a6aa-fcf1542b41b0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 12%

---

# checkAssetNames{#checkassetnames}

자산 이름을 회사의 이미지 제공/이미지 렌더링 카탈로그 네임스페이스와 모든 이름과 비교하여 IPS ID 충돌을 확인합니다.

구문

## 인증된 사용자 유형 {#section-8efcbb3f555f417a870219e4714374db}

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
| companyHandle | `xsd:string` | 아니요 | 사용자가 포함된 회사의 핸들입니다. |
| assetNamesArray | `types:StringArray` | 예 | 확인할 자산 이름의 배열입니다. |

**출력(checkAssetNamesReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| inUseNameArray | `types:StringArray` | 예 | 사용 중인 자산 이름의 배열입니다. |

## 예제 {#section-bc5d120d74614a63a425ca3acc337219}

이 샘플 코드는 지정된 회사에 대해 사용 중인 자산 이름을 요청합니다. 이 응답은 사용 중인 자산 이름의 배열을 반환합니다.

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
