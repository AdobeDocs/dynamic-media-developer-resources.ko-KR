---
description: 하나 이상의 에셋에 대한 썸네일 이미지를 설정합니다.
solution: Experience Manager
title: batchSetThumbAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f7d7ddd9-a3c3-47c4-8da6-d693851d0d7f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 11%

---

# batchSetThumbAsset{#batchsetthumbasset}

하나 이상의 에셋에 대한 썸네일 이미지를 설정합니다.

구문

## 썸네일 자산 유형 {#section-4edc2a6a8f824213b0aaddb1d437268c}

허용되는 썸네일 에셋 유형은 다음과 같이 구성됩니다.

* 이미지
* 조정된 보기
* 마스크
* 템플릿
* PsdTemplate

## 승인된 사용자 유형 {#section-5fc988e3d6384968b86fd9fe363658c0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>사용자는 대상 에셋에 대한 읽기/쓰기 액세스 권한과 썸네일 에셋에 대한 읽기 액세스 권한이 있어야 합니다.

## 매개 변수 {#section-9c6efa000b384b3db6c013def20cf40b}

**입력(batchSetThumbAssetParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 자산을 포함하는 회사에 대한 핸들입니다. |
| updateArray | `types:ThumbAssetUpdateArray` | 예 | 업데이트 배열. |

**출력(batchSetThumbAssetParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| successCount | `xsd:int` | 예 | 성공적으로 설정된 썸네일 수입니다. |
| warningCount | `xsd:int` | 예 | 작업에서 썸네일을 설정하려고 할 때 생성된 경고 수입니다. |
| errorCount | `xsd:int` | 예 | 작업에서 썸네일을 설정하려고 할 때 생성된 오류 횟수입니다. |
| warningDetailArray | `types:AssetOperationFaultArray` | 아니요 | 작업에서 업데이트를 적용하려고 할 때 경고를 생성한 자산과 관련된 세부 정보의 배열입니다. |
| errorDetailArray | `types:AssetOperationFaultArray` | 아니요 | 작업에서 업데이트를 적용하려고 할 때 오류가 발생한 자산과 관련된 세부 정보의 배열입니다. |

## 예제 {#section-6de69a8680c24c1486c5f01488393381}

**요청**

```java
<batchSetThumbAssetParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|234</assetHandle>
         <thumbAssetHandle>a|189</thumbAssetHandle>
      </items>
   </updateArray>
```

**응답**

```java
<batchSetThumbAssetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetThumbAssetReturn>
```
