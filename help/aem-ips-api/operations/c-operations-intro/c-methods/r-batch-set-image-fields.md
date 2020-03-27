---
description: 하나 이상의 이미지 자산에 대한 이미지 특정 필드를 설정합니다.
seo-description: 하나 이상의 이미지 자산에 대한 이미지 특정 필드를 설정합니다.
seo-title: batchSetImageFields
solution: Experience Manager
title: batchSetImageFields
topic: Scene7 Image Production System API
uuid: e0ad7da4-cb28-4402-8b47-a600916d23b3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# batchSetImageFields{#batchsetimagefields}

하나 이상의 이미지 자산에 대한 이미지 특정 필드를 설정합니다.

구문

## 인증된 사용자 유형 {#section-6b087bdcb7874c13acf76e113a093054}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-4969815cf67c4d11b13bb2017b3604e8}

**입력(batchSetImageFields)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 예 | 이미지 에셋이 포함된 회사의 핸들 |
| ` *`updateArray`*` | `types:ImageFieldUpdateArray` | 예 | 이미지 필드 업데이트 배열입니다. |

**출력(batchSetImageFields)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | 예 | 성공적으로 이미지 필드를 설정한 횟수입니다. |
| ` *`warningCount`*` | `xsd:int` | 예 | 작업이 이미지 필드를 설정하려고 할 때 생성된 경고 수입니다. |
| ` *`errorCount`*` | `xsd:int` | 예 | 작업이 이미지 필드를 설정하려고 할 때 생성되는 오류 수입니다. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | 아니요 | 작업이 업데이트를 적용하려고 할 때 경고를 생성한 자산과 연결된 세부 사항의 배열입니다. |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | 아니요 | 작업이 업데이트를 적용하려고 할 때 오류를 생성한 자산과 연결된 세부 사항의 배열입니다. |

## 예제 {#section-0476e3d6516a4f8bbaac9de983bc6d1e}

이 예에서는 업데이트 배열에서 두 이미지의 필드에 데이터를 설정합니다. 배열에서 이미지는 에셋 핸들에 의해 지정되고 픽셀, x 및 y 위치 앵커 좌표 및 사용자 데이터의 해상도를 포함합니다. 이 응답에는 두 이미지의 필드가 성공적으로 설정되었음을 나타냅니다.

**요청**

```java
<batchSetImageFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|140626|1|102524</assetHandle>
         <resolution>72</resolution>
         <anchorX>50</anchorX>
         <anchorY>100</anchorY>
         <userData>nada1</userData>
      </items>
      <items>
         <assetHandle>a|96680|1|64865</assetHandle>
         <resolution>150</resolution>
         <anchorX>100</anchorX>
         <anchorY>50</anchorY>
         <userData>nada2</userData>
      </items>
   </updateArray>
</batchSetImageFieldsParam>
```

**응답**

```java
<batchSetImageFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetImageFieldsReturn>
```

