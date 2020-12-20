---
description: 하나 이상의 에셋에 대한 축소판 이미지를 설정합니다.
seo-description: 하나 이상의 에셋에 대한 축소판 이미지를 설정합니다.
seo-title: batchSetThumbAsset
solution: Experience Manager
title: batchSetThumbAsset
topic: Scene7 Image Production System API
uuid: 16c298a7-bb07-4643-824b-8f864d7f0290
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 13%

---


# batchSetThumbAsset{#batchsetthumbasset}

하나 이상의 에셋에 대한 축소판 이미지를 설정합니다.

구문

## 축소판 자산 유형 {#section-4edc2a6a8f824213b0aaddb1d437268c}

허용되는 축소판 에셋 유형은 다음과 같습니다.

* 이미지
* 조정된 보기
* 마스크
* 템플릿
* PsdTemplate

## 인증된 사용자 유형 {#section-5fc988e3d6384968b86fd9fe363658c0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>사용자는 대상 자산에 대한 읽기/쓰기 액세스 권한과 축소판 자산에 대한 읽기 액세스 권한이 있어야 합니다.

## 매개 변수 {#section-9c6efa000b384b3db6c013def20cf40b}

**입력(batchSetThumbAssetParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 예 | 자산을 포함하는 회사의 핸들입니다. |
| ` *`updateArray`*` | `types:ThumbAssetUpdateArray` | 예 | 업데이트 배열입니다. |

**출력(batchSetThumbAssetParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | 예 | 성공적으로 설정된 축소판의 수입니다. |
| ` *`warningCount`*` | `xsd:int` | 예 | 작업이 축소판을 설정하려고 할 때 생성되는 경고 수입니다. |
| ` *`errorCount`*` | `xsd:int` | 예 | 작업이 축소판을 설정하려고 할 때 발생한 오류 수입니다. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | 아니요 | 작업이 업데이트를 적용하려고 할 때 경고를 생성한 자산과 연결된 세부 사항의 배열입니다. |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | 아니요 | 작업이 업데이트를 적용하려고 할 때 오류를 생성한 자산과 연결된 세부 사항의 배열입니다. |

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

