---
description: 자산을 삭제합니다.
solution: Experience Manager
title: deleteAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: dacea36e-3d40-4aaf-94fd-f0709830caf9
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 10%

---

# deleteAsset{#deleteasset}

자산을 삭제합니다.

구문

## 승인된 사용자 유형 {#section-e913be43b684491daf02bc73211e4290}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>사용자는 에셋에 대한 읽기 및 삭제 액세스 권한이 있어야 합니다.

## 매개 변수 {#section-0eed164e278b456fbdfb7a50727a0416}

**입력(deleteAssetParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 폴더가 속한 회사에 대한 핸들입니다. |
| assetHandle | `xsd:string` | 예 | 삭제할 자산에 대한 핸들입니다. |

**출력(deleteAssetParam)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-d5657289f5234bb0a613dcf691507958}

이 샘플 코드는 특정 회사에서 모든 유형의 자산을 삭제합니다. 자산 핸들이 필요하며, 이 핸들은 다른 작업에서 받아야 합니다.

**요청**

```java
<ns1:deleteAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
</ns1:deleteAssetParam>
```

**응답**

없음.
