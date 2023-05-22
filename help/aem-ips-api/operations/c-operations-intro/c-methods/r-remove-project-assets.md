---
description: 프로젝트에서 에셋을 제거합니다. 에셋을 제거하지 않습니다.
solution: Experience Manager
title: removeProjectAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 6bf169ec-c724-4ac0-a2bf-67af2ebba21a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 11%

---

# removeProjectAssets{#removeprojectassets}

프로젝트에서 에셋을 제거합니다. 에셋을 제거하지 않습니다.

구문

## 승인된 사용자 유형 {#section-b0b333a1f3b648ac8cd6bb3d135d2c6f}

* `IpsUser`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-169d8e317417415b87df86242f65710e}

**입력(removeProjectAssetsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 이동할 자산이 있는 회사에 대한 핸들입니다. |
| projectHandle | `xsd:string` | 예 | 이동할 프로젝트 자산에 대한 핸들입니다. |
| assetHandleArray | `types:HandleArray` | 예 | 이동할 자산의 핸들 배열입니다. |

**출력(removeProjectAssetsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| successCount | `xsd:int` | 예 | 자산 수를 제거했습니다. |
| warningCount | `xsd:int` | 예 | 작업에서 프로젝트에서 에셋을 제거하려고 할 때 생성된 경고 수입니다. |
| errorCount | `xsd:int` | 예 | 작업에서 프로젝트에서 에셋을 제거하려고 할 때 생성된 오류 수입니다. |
| warningDetailArray | `types:AssetOperationFaultArray` | 아니요 | 작업에서 자산을 프로젝트에서 제거하려고 할 때 경고를 생성한 자산과 관련된 세부 정보의 배열입니다. |
| errorDetailArray | `types:AssetOperationFaultArray` | 아니요 | 작업에서 프로젝트에서 에셋을 제거하려고 할 때 오류가 발생한 에셋과 관련된 세부 정보의 배열입니다. |

## 예제 {#section-13546cf0a98e4e1b91b8b7cd5724ced8}

이 코드 샘플은 프로젝트(프로젝트 핸들에 의해 지정됨)에서 2개의 자산을 제거합니다.

**요청**

```java
<removeProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|732|1|535</items>
      <items>a|739|1|537</items>
   </assetHandleArray>
</removeProjectAssetsParam>
```
