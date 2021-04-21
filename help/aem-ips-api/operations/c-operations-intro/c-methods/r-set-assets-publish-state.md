---
description: 자산 배치를 게시할 준비가 되었는지 확인합니다.
solution: Experience Manager
title: setAssetsPublishState
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 11%

---


# setAssetsPublishState{#setassetspublishstate}

자산 배치를 게시할 준비가 되었는지 확인합니다.

[setAssetState](../../../operations/c-operations-intro/c-methods/r-set-asset-publish-state.md#reference-9efc2eeea42348e0b1d5f3d1005c6563)의 일괄 버전입니다.

## 인증된 사용자 유형 {#section-0804726f683944dbbe9acfc3d35ccf25}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>사용자에게 자산에 대한 읽기 및 쓰기 액세스 권한이 있어야 합니다.

## 매개 변수 {#section-3e49d7859f8647b990d75373cc8dbc24}

**입력(setAssetsPublishStateParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 회사 핸들. |
| `*`publishStateUpdateArray`*` | `types:PublishStateUpdateArray` | 예 | 자산에 대한 게시 상태 값의 배열입니다. |

**출력(setAssetsPublishStateParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | 예 | 성공적으로 업데이트된 자산의 수입니다. |
| `*`warningCount`*` | `xsd:int` | 예 | 작업이 경고를 업데이트하려고 할 때 경고를 생성한 자산의 수입니다. |
| `*`errorCount`*` | `xsd:int` | 예 | 작업이 해당 에셋을 삭제하려고 할 때 오류를 생성한 에셋의 수입니다. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | 아니요 | 경고를 생성한 자산 업데이트와 관련된 세부 사항입니다. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | 아니요 | 오류가 발생한 자산 업데이트와 관련된 세부 사항입니다. |

## 예제 {#section-38cfdd3436214a06a1bae16875501d51}

이 코드 샘플은 자산의 게시 상태를 설정합니다.

**요청**

```java
<element name="setAssetsPublishStateParam">
   <complexType>
      <sequence>
         <element name="companyHandle" type="xsd:string"/>
         <element name="publishStateUpdateArray" type="types:PublishStateUpdateArray"/>
      </sequence>
   </complexType>
</element>
```

**응답**

```java
<element name="setAssetsPublishStateReturn">
   <complexType>
      <sequence>
         <element name="successCount" type="xsd:int"/>
         <element name="warningCount" type="xsd:int"/>
         <element name="errorCount" type="xsd:int"/>
         <element name="warningDetailArray"type="types:AssetOperationFaultArray" minOccurs="0"/>
         <element name="errorDetailArray"type="types:AssetOperationFaultArray" minOccurs="0"/>
      </sequence>
   </complexType>
</element>
```

