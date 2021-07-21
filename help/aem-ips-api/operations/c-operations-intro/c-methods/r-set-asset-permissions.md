---
description: 권한 자산을 사용하여 단일 자산의 권한을 설정합니다.
solution: Experience Manager
title: setAssetPermissions
feature: Dynamic Media Classic,SDK/API,자산 관리
role: Developer,Admin
exl-id: 1e73c305-cda5-4c30-9380-ec4cd8309933
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 9%

---

# setAssetPermissions{#setassetpermissions}

권한 자산을 사용하여 단일 자산의 권한을 설정합니다.

자산은 기본적으로 상위 폴더의 권한을 상속합니다. 자산에 대한 권한을 설정하면 `removeAssetPermissions`을 호출하지 않는 한 더 이상 상위의 권한을 상속하지 않습니다.

## 인증된 사용자 유형 {#section-91fafc170c734ed2a77beafda9221768}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-e05abbce6453450fb38747101cb5e228}

**입력(setAssetPermissionsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 작업할 폴더가 포함된 회사의 핸들입니다. |
| `*`assetHandle`*` | `xsd:string` | 예 | 폴더 핸들. |
| `*`permissionArray`*` | `types:PermissionsUpdateArray` | 예 | 권한 배열입니다. |

**출력(setAssetPermissionsReturn)**

IPS API가 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-38955bc330bb4909b6b06027ef2b143e}

이 코드 샘플은 자산에 대한 권한을 설정합니다. 여기에는 회사, 자산 핸들 및 권한 배열이 포함되어 있습니다.

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
