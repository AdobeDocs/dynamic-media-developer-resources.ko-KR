---
description: 이미지 집합을 만듭니다.
solution: Experience Manager
title: 이미지 집합 만들기
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 01ccc705-97e4-4e75-a322-e24bb78cb496
TQID: 'https://experienceleague.adobe.com/os4DfkGa5cTZfMN1vc5HeA8Qvauvwb5Q0dZ2P3HFI-c'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 136
ht-degree: 13%

---

# 이미지 집합 만들기{#createimageset}

이미지 집합을 만듭니다.

구문

## 승인된 사용자 유형 {#section-58bf5027e6d24ab5a9fcba59776d15dc}

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
| company핸들 | `xsd:string` | 예 | 이미지 세트가 속한 회사에 대한 핸들입니다. |
| folder핸들 | `xsd:string` | 예 | 폴더에 대한 핸들입니다. |
| name | `xsd:string` | 예 | 이미지 집합 이름입니다. |
| 유형 | `xsd:string` | 예 | 이미지 집합 유형입니다. |
| thumbAssetHandle | `xsd:string` | 아니요 | 새 이미지 세트의 썸네일 역할을 하는 에셋의 핸들입니다. 지정하지 않으면 IPS는 집합에 의해 참조되는 첫 번째 이미지 자산을 사용하려고 합니다. |

**출력**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| assetHandle | `xsd:string` | 예 | 새 이미지 세트에 대한 핸들입니다. |

## 예제 {#section-385fe3b0af8044b0a2451336ec137fc5}

이 코드 샘플은 회사, 폴더, 이름 및 형식으로 지정된 이미지 집합을 만듭니다. 응답은 새로 생성된 이미지 세트의 에셋 핸들입니다.

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

