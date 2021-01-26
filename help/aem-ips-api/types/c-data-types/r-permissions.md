---
description: 그룹별로 자산에 액세스, 수정, 만들기 또는 삭제할 수 있는 권한을 관리합니다.
seo-description: 그룹별로 자산에 액세스, 수정, 만들기 또는 삭제할 수 있는 권한을 관리합니다.
seo-title: 권한
solution: Experience Manager
title: 권한
topic: Dynamic Media Image Production System API
uuid: 3b3580d3-e5bc-42bf-bfbe-ab0ec2dea574
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 7%

---


# 권한{#permission}

그룹별로 자산에 액세스, 수정, 만들기 또는 삭제할 수 있는 권한을 관리합니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| `*`groupHandle`*` | `xsd:string` | 그룹 핸들. |
| `*`groupName`*` | `xsd:string` | 그룹 이름. |
| `*`permissionType`*` | `xsd:string` | 권한 유형 선택. |
| `*`isAllowed`*` | `xsd:boolean` | 권한이 허용되는지 확인합니다. |
| `*`isOverride`*` | `xsd:boolean` | 권한이 다른 권한을 재정의하는지 확인합니다. |

