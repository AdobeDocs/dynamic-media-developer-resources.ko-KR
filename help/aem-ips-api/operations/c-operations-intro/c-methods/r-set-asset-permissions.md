---
description: 권한 자산을 사용하여 단일 자산의 권한을 설정합니다.
solution: Experience Manager
title: setAssetPermissions
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 1e73c305-cda5-4c30-9380-ec4cd8309933
TQID: 'https://experienceleague.adobe.com/dd96ai2DgoCqZ1NR-2rixSHDEaBSgk6ioQIqmG-1RoE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 8%

---

# setAssetPermissions{#setassetpermissions}

권한 자산을 사용하여 단일 자산의 권한을 설정합니다.

Assets은 기본적으로 상위 폴더의 권한을 상속합니다. 에셋에 대한 권한을 설정하면 `removeAssetPermissions`을(를) 호출하지 않는 한 에셋은 더 이상 상위 에셋의 권한을 상속하지 않습니다.

## 승인된 사용자 유형 {#section-91fafc170c734ed2a77beafda9221768}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-e05abbce6453450fb38747101cb5e228}

**입력(setAssetPermissonsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 작업할 폴더가 포함된 회사에 대한 핸들입니다. |
| assetHandle | `xsd:string` | 예 | 폴더 핸들. |
| permissionArray | `types:PermissionsUpdateArray` | 예 | 권한 배열입니다. |

**출력(setAssetPermissonsReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-38955bc330bb4909b6b06027ef2b143e}

이 코드 샘플은 자산에 대한 권한을 설정합니다. 여기에는 회사 및 자산 핸들과 권한 배열이 포함됩니다.

**요청**

```java
<setAssetPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <assetHandle>97374|1|61046</assetHandle>
   <permissionArray>
      <items>
         <groupHandle>521</groupHandle>
         <permissionType>Read</permissionType>
         <isAllowed>true</isAllowed>
         <isOverride>true</isOverride>
      </items>
   </permissionArray>
</setAssetPermissionsParam>
```

**응답**

없음.

