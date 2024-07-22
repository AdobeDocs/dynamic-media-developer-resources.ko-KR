---
title: emptyAssetsFromTrash
description: IPS 휴지통에서 자산을 비웁니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 36866dc8-6a16-4445-942f-d0ea3c168272
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 6%

---

# emptyAssetsFromTrash{#emptyassetsfromtrash}

IPS 휴지통에서 자산을 비웁니다.

Assets은 수동으로 비우거나 휴지통에서 나올 때까지 휴지통에서 생활합니다. 수동으로 비우는 경우, 시스템에서 최종적으로 삭제될 다음 정리 작업(일반적으로 야간)까지 휴지통에 보관됩니다. 휴지통에서 시간이 초과되면 자산은 동일한 정리 활동의 일부로 정리됩니다. 시간 초과를 구성할 수 있습니다(기본값은 7일).

## 승인된 사용자 유형 {#section-24dee2bf5f9f4714a64955c80f2803b4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-8e1fb0ee3aae453581e99ef76e298569}

**입력(emptyAssetsFromTrashParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | xsd:string | 예 | 자산을 소유하는 회사에 대한 핸들입니다. |
| assetHandleArray | types:HandleArray | 예 | 휴지통에서 비울 항목을 나타내는 핸들의 배열입니다. |

**출력(emptyAssetsFromTrashParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| successCount | xsd:Int | 예 | 휴지통에서 성공적으로 비운 자산 수입니다. |
| warningCount | xsd:Int | 예 | 작업이 휴지통에서 자산을 비우려고 할 때 생성된 경고 수입니다. |
| errorCount | xsd:Int | 예 | 작업에서 휴지통에서 자산을 비우려고 할 때 생성된 오류 수입니다. |
| warningDetailArray | 유형:AssetOperationFaultArray | 아니요 | 작업에서 휴지통에서 비우려고 할 때 경고를 생성한 자산과 관련된 세부 정보의 배열입니다. |
| errorDetailArray | 유형:AssetOperationFaultArray | 아니요 | 작업이 휴지통에서 비우려고 할 때 오류를 생성한 에셋과 관련된 세부 정보의 배열입니다. |

## 예제 {#section-6154a873b6c342bf92e2036280cafdcf}

이 코드 샘플은 회사의 핸들과 휴지통에서 비울 자산에 대한 핸들이 포함된 자산 핸들 배열을 사용합니다.

**요청**

```java
<emptyAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2023-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</emptyAssetsFromTrashParam>
```

**응답**

```java
<emptyAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2023-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</emptyAssetsFromTrashReturn>
```
