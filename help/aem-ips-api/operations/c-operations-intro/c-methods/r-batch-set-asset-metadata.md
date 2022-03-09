---
description: 일괄 처리 모드를 사용하여 자산 메타데이터를 설정합니다.
solution: Experience Manager
title: batchSetAssetMetadata
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 7393fa4f-71fb-48a5-a7f3-91eec82c88c1
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 13%

---

# batchSetAssetMetadata{#batchsetassetmetadata}

일괄 처리 모드를 사용하여 자산 메타데이터를 설정합니다.

구문

## 인증된 사용자 유형 {#section-5310d9fd00604cbf9756944900378855}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-7111ac93bc7747f69ba14db4ac3912b0}

**입력(batchSetAssetMetadataParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| companyHandle | `xsd:string` | 예 | 배치 작업에서 설정할 메타데이터가 있는 회사의 핸들입니다. |
| updateArray | `types:BatchMetadataUpdateArray` | 예 | 자산에 적용된 메타데이터 업데이트 배열입니다. |

**출력(batchSetAssetMetadataParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| successCount | `xsd:int` | 예 | 메타데이터를 성공적으로 설정한 수입니다. |
| warningCount | `xsd:int` | 예 | 작업에서 메타데이터를 설정하려고 할 때 생성된 경고 수입니다. |
| errorCount | `xsd:int` | 예 | 작업에서 메타데이터를 설정하려고 할 때 생성된 오류 수입니다. |
| warningDetailArray | `types:AssetOperationFaultArray` | 아니요 | 자산에 대한 메타데이터를 일괄적으로 설정하려고 할 때 경고를 생성하는 자산과 연관된 세부 정보의 배열입니다. |
| errorDetailArray | `types:AssetOperationFaultArray` | 아니요 | 자산에 대한 메타데이터를 일괄적으로 설정하려고 할 때 오류를 생성하는 자산과 연관된 세부 사항의 배열입니다. |

## 예제 {#section-2de798ac920e4b47b971b1729a64395b}

**요청**

```java
<batchSetAssetMetadataParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
<companyHandle>c|6</companyHandle>
<updateArray>
   <items>
      <assetHandleArray>
         <items>a|743|1|538</items>
         <items>a|744|1|539</items>
      </assetHandleArray>
      <updateArray>
         <items>
            <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
            <value>400</value>
         </items>
      </updateArray>
   </items>
   <items>
      <assetHandleArray>
         <items>a|732|1|535</items>
         <items>a|739|1|537</items>
      </assetHandleArray>
      <updateArray>
         <items>
            <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
            <value>300</value>
         </items>
      </updateArray>
   </items>
</updateArray>
</batchSetAssetMetadataParam>
```

**응답**

```java
<batchSetAssetMetadataReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>4</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetAssetMetadataReturn>
```
