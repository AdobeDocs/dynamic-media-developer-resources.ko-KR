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
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 7%

---


# emptyAssetsFromTrash{#emptyassetsfromtrash}

IPS 휴지통에서 에셋을 비웁니다.

에셋은 휴지통에서 수동으로 비워두거나 휴지통을 벗어날 때까지 그대로 유지됩니다. 수동으로 빈 경우 시스템에서 마지막으로 제거될 때 다음 정리 작업(일반적으로 밤낮)까지 휴지통에 둡니다. 휴지통에서 시간이 나면, 자산은 동일한 정리 활동의 일부로서 정리됩니다. 시간 초과는 구성 가능합니다(기본값은 7일).

## 인증된 사용자 유형 {#section-24dee2bf5f9f4714a64955c80f2803b4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* &quot;

## 매개 변수 {#section-8e1fb0ee3aae453581e99ef76e298569}

**입력(emptyAssetsFromTrashParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 예 | 자산을 소유한 회사의 핸들입니다. |
| ` *`assetHandleArray`*` | `types:HandleArray` | 예 | 휴지통에서 비울 항목을 나타내는 핸들 배열입니다. |

**출력(emptyAssetsFromTrashParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`successCount`*` | `xsd:Int` | 예 | 휴지통에서 성공적으로 비운 자산 수입니다. |
| ` *`warningCount`*` | `xsd:Int` | 예 | 작업에서 휴지통에서 자산을 비우기 시도할 때 생성된 경고 수입니다. |
| ` *`errorCount`*` | `xsd:Int` | 예 | 작업에서 휴지통에서 자산을 비울 때 생성된 오류 수입니다. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | 아니요 | 작업에서 휴지통에서 경고를 제거하려고 할 때 경고를 생성한 자산과 연관된 세부 사항의 배열입니다. |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | 아니요 | 작업에서 휴지통에서 오류를 제거하려고 할 때 오류가 발생한 자산과 연관된 세부 사항의 배열입니다. |

## 예제 {#section-6154a873b6c342bf92e2036280cafdcf}

이 코드 샘플에서는 휴지통에서 비워둘 에셋에 대한 핸들이 들어 있는 회사 핸들 및 에셋 핸들 배열을 사용합니다.

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

