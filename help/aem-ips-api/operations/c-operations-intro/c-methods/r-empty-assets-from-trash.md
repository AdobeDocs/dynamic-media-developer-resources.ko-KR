---
description: IPS 휴지통에서 에셋을 비웁니다.
seo-description: IPS 휴지통에서 에셋을 비웁니다.
seo-title: emptyAssetsFromTrash
solution: Experience Manager
title: emptyAssetsFromTrash
topic: Scene7 Image Production System API
uuid: de11a7b0-cd4b-4717-8596-d39afbcf7e9c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# emptyAssetsFromTrash{#emptyassetsfromtrash}

IPS 휴지통에서 에셋을 비웁니다.

에셋은 수동으로 비워지거나 휴지통에서 시간이 초과될 때까지 휴지통에 그대로 유지됩니다. 수동으로 비울 경우 다음 정리 작업(일반적으로 매일 밤)이 최종적으로 시스템에서 제거될 때까지 휴지통에 둡니다. 휴지통에서 시간이 초과되면, 자산은 동일한 정리 활동의 일부로 정리됩니다. 시간 초과는 구성 가능합니다(기본값은 7일).

## 인증된 사용자 유형 {#section-24dee2bf5f9f4714a64955c80f2803b4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* ``

## 매개 변수 {#section-8e1fb0ee3aae453581e99ef76e298569}

**입력(emptyAssetsFromTrashParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 예 | 자산을 소유한 회사의 핸들 |
| ` *`assetHandleArray`*` | `types:HandleArray` | 예 | 휴지통에서 비울 항목을 나타내는 핸들 배열입니다. |

**출력(emptyAssetsFromTrashParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`successCount`*` | `xsd:Int` | 예 | 휴지통에서 성공적으로 비운 자산 수입니다. |
| ` *`warningCount`*` | `xsd:Int` | 예 | 작업에서 휴지통에서 자산을 비우려고 할 때 생성된 경고 수입니다. |
| ` *`errorCount`*` | `xsd:Int` | 예 | 작업에서 휴지통에서 자산을 비우려고 할 때 생성되는 오류 수입니다. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | 아니요 | 작업에서 휴지통에서 경고를 생성했을 때 경고를 생성한 자산과 관련된 세부 사항의 배열입니다. |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | 아니요 | 작업에서 휴지통에서 오류를 제거하려고 할 때 오류를 생성한 자산과 연결된 세부 사항의 배열입니다. |

## 예제 {#section-6154a873b6c342bf92e2036280cafdcf}

이 코드 샘플에서는 휴지통에서 비울 자산에 대한 핸들이 들어 있는 회사 핸들 및 자산 핸들 배열을 사용합니다.

**요청**

```java
<emptyAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</emptyAssetsFromTrashParam>
```

**응답**

```java
<emptyAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</emptyAssetsFromTrashReturn>
```

