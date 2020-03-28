---
description: 자산 권한을 업데이트합니다.
seo-description: 자산 권한을 업데이트합니다.
seo-title: updateAssetPermissions
solution: Experience Manager
title: updateAssetPermissions
topic: Scene7 Image Production System API
uuid: feb2faf3-81de-436e-82de-1e41df03508f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# updateAssetPermissions{#updateassetpermissons}

자산 권한을 업데이트합니다.

구문

## 인증된 사용자 유형 {#section-3928e9badc3842e1859af4ed362df719}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-392cb3076cf84790a32fd913f2b111a3}

**입력(updateAssetPermissionsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 예 | 회사 핸들 |
| ` *`assetHandle`*` | `xsd:string` | 예 | 자산 핸들. |
| ` *`updateArray`*` | `types:PermissionUpdateArray` | 예 | 자산에 적용할 권한. |

**출력(updateAssetPermissionsReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-1b7b7dbfdab34c819a53f3d33004e1f9}

**요청**

```java
<ns1:updateAssetPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>15674|25|1062</ns1:assetHandle>
   <ns1:updateArray>
      <ns1:items>
         <ns1:groupHandle>225</ns1:groupHandle>
         <ns1:permissionType>Read</ns1:permissionType>
         <ns1:isAllowed>true</ns1:isAllowed>
         <ns1:isOverride>false</ns1:isOverride>
      </ns1:items>
   </ns1:updateArray>
</ns1:updateAssetPermissionsParam>
```

**응답**

없음.
