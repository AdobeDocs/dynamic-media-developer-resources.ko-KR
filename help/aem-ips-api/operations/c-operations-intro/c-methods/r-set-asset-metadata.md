---
description: 자산에 대한 메타데이터 값을 설정합니다. 메타데이터 업데이트 배열로 작업하여 값을 일괄적으로 설정할 수 있습니다.
seo-description: 자산에 대한 메타데이터 값을 설정합니다. 메타데이터 업데이트 배열로 작업하여 값을 일괄적으로 설정할 수 있습니다.
seo-title: setAssetMetadata
solution: Experience Manager
title: setAssetMetadata
topic: Dynamic Media Image Production System API
uuid: 17fe8277-a164-4f91-af96-ea43d41bd4f2
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 9%

---


# setAssetMetadata{#setassetmetadata}

자산에 대한 메타데이터 값을 설정합니다. 메타데이터 업데이트 배열로 작업하여 값을 일괄적으로 설정할 수 있습니다.

구문

## 인증된 사용자 유형 {#section-9dcacb0c924044648f8324bfed183dca}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>사용자에게 자산에 대한 읽기 권한이 있어야 합니다.

## 매개 변수 {#section-bcdcff30905e444388811e897b2824bd}

**입력(setAssetMetadataParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 업데이트할 자산이 있는 회사에 대한 핸들입니다. |
| `*`assetHandle`*` | `xsd:string` | 예 | 자산의 핸들입니다. |
| `*`updateArray`*` | `types:MetadataUpdateArray` | 예 | 메타데이터 업데이트 배열에서 업데이트합니다. |

**출력(setAssetMetadataReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-1ab412e7ee1d4d6d8469b0b403598c42}

이 코드 샘플은 메타데이터 업데이트 배열을 사용하여 지정된 자산의 메타데이터를 설정합니다.

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
