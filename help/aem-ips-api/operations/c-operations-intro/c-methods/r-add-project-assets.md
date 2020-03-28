---
description: 프로젝트에 하나 이상의 자산을 추가합니다.
seo-description: 프로젝트에 하나 이상의 자산을 추가합니다.
seo-title: addProjectAssets
solution: Experience Manager
title: addProjectAssets
topic: Scene7 Image Production System API
uuid: 48abea17-058e-4469-bb16-0abee8ef5214
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# addProjectAssets{#addprojectassets}

프로젝트에 하나 이상의 자산을 추가합니다.

구문

## 인증된 사용자 유형 {#section-c67e7422921047f4ab4d4e9ba5a7aafe}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-20d498e971b6466298e60c8a77fc32b2}

**입력(addProjectAssetsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 예 | 현재 프로젝트와 연결된 회사를 처리합니다. |
| ` *`projectHandle`*` | `xsd:string` | 예 | 자산을 추가할 프로젝트를 처리합니다. |
| ` *`projectHandleArray`*` | `xsd:HandleArray` | 예 | 현재 프로젝트에 추가할 자산의 배열입니다. |

**출력(addProjectAssetsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | 예 | 추가된 자산의 수입니다. |
| ` *`warningCount`*` | `xsd:int` | 예 | 작업이 프로젝트에 자산을 추가하려고 할 때 생성된 경고 수입니다. |
| ` *`errorCount`*` | `xsd:int` | 예 | 작업이 프로젝트에 자산을 추가하려고 할 때 생성되는 오류 수입니다. |
| ` *`warningDetailHandle`*` | `xsd:AssetOperationFaultArray` | 아니요 | 작업이 프로젝트에 자산을 추가하려고 할 때 자산에서 생성된 경고 배열입니다. |
| ` *`companyHandle`*` | `xsd:AssetOperationFaultArray` | 아니요 | 작업이 프로젝트에 에셋을 추가하려고 할 때 에셋에 의해 생성된 오류 배열입니다. |

## 예제 {#section-bee5be2402f54cb9a3a02cc07def4135}

이 예에서는 자산 핸들 배열의 단일 자산(핸들에서 참조됨)을 요청에 지정된 프로젝트에 추가합니다. 응답이 `successCount` 반환되면 작업이 성공적으로 완료되었습니다 `1`.

**요청**

```java
<addProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|732|1|535</items>
   </assetHandleArray>
</addProjectAssetsParam>
```

**응답**

```java
<addProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</addProjectAssetsReturn>
```

