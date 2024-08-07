---
description: 선택한 자산에서 권한을 제거합니다.
solution: Experience Manager
title: removeAssetPermissions
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c47d9853-91b1-45fe-b8ff-aaa1239ca0d1
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 14%

---

# removeAssetPermissions{#removeassetpermissions}

선택한 자산에서 권한을 제거합니다.

구문

## 승인된 사용자 유형 {#section-239058fdb4454e519ac327e621cb3abc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-b70bf3b033ca45b396964baf2ab1fb0f}

**입력(removeAssetPermissionsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 회사 손잡이. |
| assetHandle | `xsd:string` | 예 | 제거할 권한이 있는 자산에 대한 핸들입니다. |

**출력(removeAssetPermissionsReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-238fa7bb091548f5ba72ced11fc92d4f}

이 코드 샘플은 에셋에서 권한을 제거합니다.

**요청**

```java
<ns1:removeAssetPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>15674|25|1062</ns1:assetHandle>
</ns1:removeAssetPermissionsParam>
```

**응답**

없음.
