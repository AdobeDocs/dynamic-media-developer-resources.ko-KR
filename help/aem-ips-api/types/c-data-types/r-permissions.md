---
description: 그룹별로 자산에 액세스, 수정, 만들기 또는 삭제할 권한을 관리합니다.
solution: Experience Manager
title: 권한
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 18e5f8f6-3cbe-4d36-b02a-5a3002e4498c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 9%

---

# 권한{#permission}

그룹별로 자산에 액세스, 수정, 만들기 또는 삭제할 권한을 관리합니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| groupHandle | `xsd:string` | 그룹 핸들. |
| groupName | `xsd:string` | 그룹 이름. |
| permissionType | `xsd:string` | 권한 유형을 선택합니다. |
| isAllowed | `xsd:boolean` | 권한이 허용되는지 확인합니다. |
| isOverride | `xsd:boolean` | 권한이 다른 권한을 재정의하는지 여부를 결정합니다. |
