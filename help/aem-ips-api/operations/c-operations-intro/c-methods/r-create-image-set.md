---
description: 이미지 세트를 만듭니다.
solution: Experience Manager
title: createImageSet
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 01ccc705-97e4-4e75-a322-e24bb78cb496
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 15%

---

# createImageSet{#createimageset}

이미지 세트를 만듭니다.

구문

## 인증된 사용자 유형 {#section-58bf5027e6d24ab5a9fcba59776d15dc}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>사용자는 대상 폴더에 대한 읽기/쓰기 액세스 권한이 있어야 합니다.

## 매개 변수 {#section-03d22ba7d290477e91c25ca1d4439200}

**입력(createImageSetParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| companyHandle | `xsd:string` | 예 | 이미지 세트가 속한 회사의 핸들입니다. |
| folderHandle | `xsd:string` | 예 | 폴더에 대한 핸들입니다. |
| 이름 | `xsd:string` | 예 | 이미지 세트 이름입니다. |
| 유형 | `xsd:string` | 예 | 이미지 세트 유형입니다. |
| thumbAssetHandle | `xsd:string` | 아니요 | 새 이미지 세트의 축소판 역할을 하는 자산의 처리합니다. 지정하지 않으면 IPS는 세트에서 참조하는 첫 번째 이미지 자산을 사용합니다. |

**출력**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| assetHandle | `xsd:string` | 예 | 새 이미지 세트에 대한 핸들입니다. |

## 예제 {#section-385fe3b0af8044b0a2451336ec137fc5}

이 코드 샘플은 회사, 폴더, 이름 및 유형별로 지정된 이미지 세트를 만듭니다. 응답은 새로 만든 이미지 세트의 자산 핸들입니다.

**요청**

```java
<ns1:createImageSetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/eCatalogs/</ns1:folderHandle>
   <ns1:name>My Image Set</ns1:name>
   <ns1:type>ImageSet</ns1:type>
</ns1:createImageSetParam>
```

**응답**

```java
<createImageSetReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <assetHandle>25741|22|841</assetHandle>
</createImageSetReturn>
```
