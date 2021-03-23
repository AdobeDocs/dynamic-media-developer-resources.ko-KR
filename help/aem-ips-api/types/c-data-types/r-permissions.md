---
description: 그룹별로 자산에 액세스, 수정, 만들기 또는 삭제할 수 있는 권한을 관리합니다.
seo-description: 그룹별로 자산에 액세스, 수정, 만들기 또는 삭제할 수 있는 권한을 관리합니다.
seo-title: 권한
solution: Experience Manager
title: 권한
uuid: 3b3580d3-e5bc-42bf-bfbe-ab0ec2dea574
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 6%

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

