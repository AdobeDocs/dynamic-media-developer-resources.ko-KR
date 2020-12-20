---
description: 권한 자산을 사용하여 단일 자산의 권한을 설정합니다.
seo-description: 권한 자산을 사용하여 단일 자산의 권한을 설정합니다.
seo-title: setAssetPermissions
solution: Experience Manager
title: setAssetPermissions
topic: Scene7 Image Production System API
uuid: 38f26482-bce9-4d2c-9714-e8c3ae40c2d1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 8%

---


# setAssetPermissions{#setassetpermissions}

권한 자산을 사용하여 단일 자산의 권한을 설정합니다.

자산은 기본적으로 상위 폴더의 권한을 상속합니다. 자산에 대한 권한을 설정하면 `removeAssetPermissions`을(를) 호출하지 않는 한 더 이상 해당 부모의 권한을 상속하지 않습니다.

## 인증된 사용자 유형 {#section-91fafc170c734ed2a77beafda9221768}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-e05abbce6453450fb38747101cb5e228}

**입력(setAssetPermissonsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 예 | 작업할 폴더가 포함된 회사의 핸들입니다. |
| ` *`assetHandle`*` | `xsd:string` | 예 | 폴더 핸들. |
| ` *`permissionArray`*` | `types:PermissionsUpdateArray` | 예 | 사용 권한 배열로 이동합니다. |

**출력(setAssetPermissonsReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-38955bc330bb4909b6b06027ef2b143e}

이 코드 샘플은 자산에 대한 권한을 설정합니다. 여기에는 회사 및 자산 핸들 및 권한 배열이 포함됩니다.

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
