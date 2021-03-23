---
description: 폴더 권한을 설정합니다.
seo-description: 폴더 권한을 설정합니다.
seo-title: setFolderPermissions
solution: Experience Manager
title: setFolderPermissions
uuid: 3a33034e-df2c-48ab-8ade-b76bea444388
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 13%

---


# setFolderPermissions{#setfolderpermissions}

폴더 권한을 설정합니다.

구문

## 인증된 사용자 유형 {#section-d3eb923fcf5741b99967634db809e09e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-2a41135054954396b40f1228f2e63b42}

**입력(setFolderPermissionsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 회사 핸들. |
| `*`folderHandle`*` | `xsd:string` | 예 | 폴더 핸들. |
| `*`setChildren`*` | `xsd:boolean` | 예 | 폴더에 속하는 하위 항목에 대한 권한을 설정합니다. |
| `*`permissionArray`*` | `types:PermissionUpdateArray` | 예 | 사용 권한 배열로 이동합니다. |

**출력(setFolderPermissionsReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-01730da4be874553ab44e3241cdf6357}

이 코드 샘플은 회사 핸들, 폴더 핸들 및 폴더에 대한 자세한 정보가 있는 권한 배열을 지정합니다. 상위 폴더의 하위 폴더에 대해 동일한 권한을 적용합니다.

**요청**

```java
<setFolderPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <folderHandle>blackmesa/Awatermark/</folderHandle>
   <setChildren>true</setChildren>
   <permissionArray>
      <items>
         <groupHandle>521</groupHandle>
         <permissionType>Read</permissionType>
         <isAllowed>true</isAllowed>
         <isOverride>true</isOverride>
      </items>
   </permissionArray>
</setFolderPermissionsParam>
```

**응답**

없음.
