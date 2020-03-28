---
description: 하나 이상의 자산에 대한 게시 상태를 설정하거나 업데이트합니다. 회사의 각 게시 컨텍스트에 대해 별도의 게시 상태를 설정할 수 있습니다.
seo-description: 하나 이상의 자산에 대한 게시 상태를 설정하거나 업데이트합니다. 회사의 각 게시 컨텍스트에 대해 별도의 게시 상태를 설정할 수 있습니다.
seo-title: setAssetsContextState
solution: Experience Manager
title: setAssetsContextState
topic: Scene7 Image Production System API
uuid: 4b94f9ea-3f7b-45ee-9381-6434f2bc4e31
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
>사용자에게 자산을 반환하려면 읽기 권한이 있어야 합니다.

## 매개 변수 {#section-009b9006de8e4c16ad657c47f28ace9f}

**입력(set 파섹**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 예 | 회사를 담당하세요. |
| ` *`assetsContextHandle`*` | `types:AssetsContextStateUpdateArray` | 예 | 자산 및 새 게시 상태의 배열입니다. |

**출력(set 파섹**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | 예 | 자산 수가 변경되었습니다. |
| ` *`warningCount`*` | `xsd:int` | 예 | 작업이 자산을 수정하려고 할 때 생성된 경고 수입니다. |
| ` *`errorCount`*` | `xsd:int` | 예 | 작업이 자산을 수정하려고 할 때 생성된 오류 수입니다. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | 아니요 | 작업이 수정하려고 할 때 자산에서 생성된 오류 배열입니다. |

## 예제 {#section-283a073f3cb14bcda5abed863c538aa4}

이 코드 샘플은 를 사용하여 자산의 게시 상태를 설정합니다 `NotMarkedForPublish`.

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

