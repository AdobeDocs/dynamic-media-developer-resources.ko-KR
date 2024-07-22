---
description: 에셋의 메타데이터 값을 설정합니다. 일괄 처리에서 값을 설정하는 메타데이터 업데이트 배열에서 작동합니다.
solution: Experience Manager
title: setAssetMetadata
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 811e44e1-774a-49bd-a2bd-a7504e5f7f5f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 8%

---

# setAssetMetadata{#setassetmetadata}

에셋의 메타데이터 값을 설정합니다. 일괄 처리에서 값을 설정하는 메타데이터 업데이트 배열에서 작동합니다.

구문

## 승인된 사용자 유형 {#section-9dcacb0c924044648f8324bfed183dca}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>사용자는 에셋에 대한 읽기 액세스 권한이 있어야 합니다.

## 매개 변수 {#section-bcdcff30905e444388811e897b2824bd}

**입력(setAssetMetadataParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 업데이트할 자산이 있는 회사에 대한 핸들입니다. |
| assetHandle | `xsd:string` | 예 | 에셋에 대한 핸들입니다. |
| updateArray | `types:MetadataUpdateArray` | 예 | 메타데이터 업데이트 배열의 업데이트입니다. |

**출력(setAssetMetadataReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-1ab412e7ee1d4d6d8469b0b403598c42}

이 코드 샘플은 메타데이터 업데이트 배열을 사용하여 지정된 에셋의 메타데이터를 설정합니다.

**요청**

```java
<ns1:setAssetMetadataParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
   <ns1:updateArray>
      <ns1:items>
         <ns1:fieldHandle>47|ALL|Resolution</ns1:fieldHandle>
         <ns1:value>320</ns1:value>
      </ns1:items>
   </ns1:updateArray>
</ns1:setAssetMetadataParam>
```

**응답**

없음.
