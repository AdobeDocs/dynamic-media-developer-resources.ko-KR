---
description: 폴더 권한을 업데이트합니다.
solution: Experience Manager
title: updateFolderPermissions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 4e4f382e-4339-4b9d-a721-d33a4fa8be6b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 19%

---

# updateFolderPermissions{#updatefolderpermissions}

폴더 권한을 업데이트합니다.

구문

## 승인된 사용자 유형 {#section-e5c2217231bf4b3386e0ab3f2e9aca0b}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-339e6e17c5504e1ea79fbdc05f618050}

**입력(updateFolderPermissionsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 회사 핸들. |
| folder핸들 | `xsd:string` | 예 | 폴더 핸들. |
| updateChills | `xsd:boolean` | 예 | 최상위 폴더에 설정된 권한으로 하위 항목을 업데이트할지 여부를 결정합니다. |
| updateArray | `types:PermissionUpdateArray` | 예 | 폴더에 적용할 권한 업데이트의 배열입니다. |

**출력(updateFolderPermissionsReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-c3fe4d4388674870a3856c35ef66b631}

**요청**

```java
<ns1:updateFolderPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/eCatalogs/</ns1:folderHandle>
   <ns1:updateChildren>false</ns1:updateChildren>
   <ns1:updateArray>
      <ns1:items>
         <ns1:groupHandle>225</ns1:groupHandle>
         <ns1:permissionType>Read</ns1:permissionType>
         <ns1:isAllowed>true</ns1:isAllowed>
         <ns1:isOverride>true</ns1:isOverride>
      </ns1:items>
   </ns1:updateArray>
</ns1:updateFolderPermissionsParam>
```

**응답**

없음.
