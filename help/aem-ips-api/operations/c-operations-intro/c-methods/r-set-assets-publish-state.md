---
description: 자산 배치를 게시할 준비가 되었는지 여부를 결정합니다.
solution: Experience Manager
title: setAssetsPublishState
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: dce324e4-cf86-4a65-ab00-8cd2bba20f8f
TQID: 'https://experienceleague.adobe.com/VV11khRodimEOAdPB-6mHR-gIT4AMiKOKeuuH6J15VA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 151
ht-degree: 11%

---

# setAssetsPublishState{#setassetspublishstate}

자산 배치를 게시할 준비가 되었는지 여부를 결정합니다.

[setAssetState](../../../operations/c-operations-intro/c-methods/r-set-asset-publish-state.md#reference-9efc2eeea42348e0b1d5f3d1005c6563)의 일괄 처리 버전입니다.

## 승인된 사용자 유형 {#section-0804726f683944dbbe9acfc3d35ccf25}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>사용자에게 에셋에 대한 읽기 및 쓰기 권한이 있어야 합니다.

## 매개 변수 {#section-3e49d7859f8647b990d75373cc8dbc24}

**입력(setAssetsPublishStateParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 회사 핸들. |
| publishStateUpdateArray | `types:PublishStateUpdateArray` | 예 | 자산에 대한 게시 상태 값의 배열입니다. |

**출력(setAssetsPublishStateParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| successCount | `xsd:int` | 예 | 성공적으로 업데이트된 에셋 수 |
| warningCount | `xsd:int` | 예 | 작업에서 자산 업데이트를 시도할 때 경고를 생성한 자산 수입니다. |
| errorCount | `xsd:int` | 예 | 작업에서 오류를 삭제하려고 할 때 오류가 발생한 자산 수입니다. |
| warningDetailArray | `types:AssetOperationFaultArray` | 아니요 | 경고를 생성한 자산 업데이트와 관련된 세부 정보. |
| errorDetailArray | `types:AssetOperationFaultArray` | 아니요 | 오류를 생성한 자산 업데이트와 관련된 세부 정보. |

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

