---
description: 하나 이상의 자산에 대한 게시 상태를 설정하거나 업데이트합니다. 회사의 각 게시 컨텍스트에 대해 별도의 게시 상태를 설정할 수 있습니다.
solution: Experience Manager
title: setAssetsContextState
feature: Dynamic Media Classic,SDK/API,자산 관리
role: Developer,Admin
exl-id: 28d0a67b-3e36-43fc-800d-17c841dca3a0
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 10%

---

# setAssetsContextState{#setassetscontextstate}

하나 이상의 자산에 대한 게시 상태를 설정하거나 업데이트합니다. 회사의 각 게시 컨텍스트에 대해 별도의 게시 상태를 설정할 수 있습니다.

## 인증된 사용자 유형 {#section-815eb031f85143278c1560c18c5e3431}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>자산을 반환하려면 사용자에게 읽기 권한이 있어야 합니다.

## 매개 변수 {#section-009b9006de8e4c16ad657c47f28ace9f}

**입력(setAssetsContextStateParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 회사를 담당합니다. |
| `*`assetsContextHandle`*` | `types:AssetsContextStateUpdateArray` | 예 | 자산 및 새 게시 상태의 배열입니다. |

**출력(setAssetsContextStateReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | 예 | 자산 수가 변경되었습니다. |
| `*`warningCount`*` | `xsd:int` | 예 | 작업이 자산을 수정하려고 할 때 생성된 경고 수입니다. |
| `*`errorCount`*` | `xsd:int` | 예 | 작업이 자산을 수정하려고 할 때 생성된 오류 수입니다. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | 아니요 | 작업에서 자산을 수정하려고 할 때 자산에서 생성된 오류 배열입니다. |

## 예제 {#section-283a073f3cb14bcda5abed863c538aa4}

이 코드 샘플은 `NotMarkedForPublish`을 사용하여 자산의 게시 상태를 설정합니다.

**요청**

```java
<setAssetsContextStateParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <companyHandle>c|301</companyHandle>
  <assetsContextStateUpdateArray>
    <items>
      <assetHandle>a|27007</assetHandle>
      <contextStateUpdateArray>
        <items>
          <contextHandle>pc|3001</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3002</contextHandle>
          <publishState>MarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3003</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3004</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
      </contextStateUpdateArray>
    </items>
    <items>
      <assetHandle>a|27008</assetHandle>
      <contextStateUpdateArray>
        <items>
          <contextHandle>pc|3001</contextHandle>
          <publishState>MarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3002</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3003</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3004</contextHandle>
          <publishState>MarkedForPublish</publishState>
        </items>
      </contextStateUpdateArray>
    </items>
  </assetsContextStateUpdateArray>
</setAssetsContextStateParam>
```

**응답**

```java
<setAssetsContextStateReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04-beta">
  <successCount>8</successCount>
  <warningCount>0</warningCount>
  <errorCount>0</errorCount>
</setAssetsContextStateReturn>
```
