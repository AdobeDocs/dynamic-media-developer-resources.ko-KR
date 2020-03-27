---
description: 휴지통에서 자산을 복원합니다.
seo-description: 휴지통에서 자산을 복원합니다.
seo-title: restoreAssetsFromTrash
solution: Experience Manager
title: restoreAssetsFromTrash
topic: Scene7 Image Production System API
uuid: f7424d4c-7807-4de9-ad0c-f96364bf7b82
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# restoreAssetsFromTrash{#restoreassetsfromtrash}

휴지통에서 자산을 복원합니다.

구문

## 인증된 사용자 유형 {#section-15e887782c7d4ace897ff02c6ad5baa0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-200a61d040c94e489a85241b29cd499a}

**입력(restoreAssetsFromTrashParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 예 | 복원할 자산이 있는 회사의 핸들 |
| ` *`assetHandleArray`*` | `types:HandleArray` | 예 | 복원할 자산의 핸들 배열입니다. |

**출력(restoreAssetsFromTrashReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | 예 | 휴지통에서 성공적으로 제거된 자산 수입니다. |
| ` *`warningCount`*` | `xsd:int` | 예 | 작업에서 휴지통에서 자산을 복원하려고 할 때 생성된 경고 수입니다. |
| ` *`errorCount`*` | `xsd:int` | 예 | 휴지통에서 자산을 복원하려고 할 때 생성된 오류 수입니다. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | 아니요 | 작업에서 휴지통에서 자산을 복원하려고 할 때 경고를 생성한 자산과 관련된 세부 사항의 배열입니다. |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | 아니요 | 작업에서 휴지통에서 자산을 복원하려고 할 때 오류를 생성한 자산과 관련된 세부 사항의 배열입니다. |

## 예제 {#section-98fe0394b0634ca397c395f14f8a9358}

이 코드 샘플은 휴지통에서 자산을 복원합니다. 응답은 작업이 성공적으로 완료되었음을 나타냅니다.

**요청**

```java
<restoreAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</restoreAssetsFromTrashParam>
```

**응답**

```java
<restoreAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</restoreAssetsFromTrashReturn
```

