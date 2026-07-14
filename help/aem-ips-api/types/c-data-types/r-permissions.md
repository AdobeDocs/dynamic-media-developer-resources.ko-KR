---
description: 그룹별로 에셋에 대한 액세스, 수정, 생성 또는 삭제 권한을 관리합니다.
solution: Experience Manager
title: 권한
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 18e5f8f6-3cbe-4d36-b02a-5a3002e4498c
TQID: 'https://experienceleague.adobe.com/BfB4MGiJFqPkJqL26YSmrhd52KfxhVX5TC-LHxEhevo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 53
ht-degree: 9%

---

# [!DNL Permission]{#permission}

그룹별로 에셋에 대한 액세스, 수정, 생성 또는 삭제 권한을 관리합니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| group핸들 | `xsd:string` | 그룹 핸들. |
| groupName | `xsd:string` | 그룹 이름. |
| permissionType | `xsd:string` | 권한 유형 선택. |
| isAllow | `xsd:boolean` | 사용 권한이 허용되는지 여부를 결정합니다. |
| isOverride | `xsd:boolean` | 권한이 다른 권한을 재정의하는지 여부를 결정합니다. |

