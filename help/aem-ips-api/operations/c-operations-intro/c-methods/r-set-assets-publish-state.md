---
description: 자산 묶음을 게시할 준비가 되었는지 확인합니다.
seo-description: 자산 묶음을 게시할 준비가 되었는지 확인합니다.
seo-title: setAssetsPublishState
solution: Experience Manager
title: setAssetsPublishState
topic: Scene7 Image Production System API
uuid: 2910cd6c-573b-405c-864d-a0136ac5472d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAssetsPublishState{#setassetspublishstate}

자산 묶음을 게시할 준비가 되었는지 확인합니다.

setAssetState의 일괄 [버전입니다](../../../operations/c-operations-intro/c-methods/r-set-asset-publish-state.md#reference-9efc2eeea42348e0b1d5f3d1005c6563).

## 인증된 사용자 유형 {#section-0804726f683944dbbe9acfc3d35ccf25}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>사용자는 자산에 대한 읽기 및 쓰기 액세스 권한이 있어야 합니다.

## 매개 변수 {#section-3e49d7859f8647b990d75373cc8dbc24}

**입력(set 파섹**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 예 | 회사 핸들 |
| ` *`publish 파섹`*` | `types:PublishStateUpdateArray` | 예 | 자산에 대한 게시 상태 값의 배열입니다. |

**출력(set 파섹**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | 예 | 성공적으로 업데이트된 자산의 수입니다. |
| ` *`warningCount`*` | `xsd:int` | 예 | 작업 시 경고를 생성한 자산의 수입니다. |
| ` *`errorCount`*` | `xsd:int` | 예 | 작업이 오류를 삭제하려고 할 때 오류를 생성한 자산의 수입니다. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | 아니요 | 경고를 생성한 자산 업데이트와 관련된 세부 사항입니다. |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | 아니요 | 오류를 생성한 자산 업데이트와 관련된 세부 사항입니다. |

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

