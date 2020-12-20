---
description: 자산을 삭제합니다.
seo-description: 자산을 삭제합니다.
seo-title: deleteAsset
solution: Experience Manager
title: deleteAsset
topic: Scene7 Image Production System API
uuid: 47f700e0-04bf-4d33-a18a-d938f7e9e326
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 12%

---


# deleteAsset{#deleteasset}

자산을 삭제합니다.

구문

## 인증된 사용자 유형 {#section-e913be43b684491daf02bc73211e4290}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>사용자에게 자산에 대한 읽기 및 삭제 액세스 권한이 있어야 합니다.

## 매개 변수 {#section-0eed164e278b456fbdfb7a50727a0416}

**입력(deleteAssetParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 예 | 폴더가 속하는 회사의 핸들입니다. |
| ` *`assetHandle`*` | `xsd:string` | 예 | 삭제할 자산의 핸들입니다. |

**출력(deleteAssetParam)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-d5657289f5234bb0a613dcf691507958}

이 샘플 코드는 특정 회사에서 자산 유형을 삭제합니다. 다른 작업에서 얻어야 하는 자산 핸들이 필요합니다.

**요청**

```java
<ns1:deleteAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
</ns1:deleteAssetParam>
```

**응답**

없음.
