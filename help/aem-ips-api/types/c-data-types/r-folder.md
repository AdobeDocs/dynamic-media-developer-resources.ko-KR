---
description: 계층 구조 파일 또는 자산 저장소 개체입니다. 폴더에는 하나 이상의 하위 폴더가 포함될 수 있습니다.
solution: Experience Manager
title: 폴더
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 74b44b1a-a92e-4c97-a93b-0cd4552f78ec
TQID: 'https://experienceleague.adobe.com/nh6zqOnt-bxAFmsHSHPRCMThKlOwi-9b9fep6ujKZyE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 70
ht-degree: 8%

---

# [!DNL Folder]{#folder}

계층 구조 파일 또는 자산 저장소 개체입니다. 폴더에는 하나 이상의 하위 폴더가 포함될 수 있습니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| folder핸들 | `xsd:string` | 폴더 핸들. |
| [!DNL path] | `xsd:string` | 폴더 경로. |
| 마지막 수정일 | `xsd:dateTime` | 마지막 수정 날짜. |
| childLastModified | `xsd:dateTime` | 하위 폴더 및 폴더 하위 자산의 마지막 수정 날짜입니다. |
| permissionsSetHandle | `xsd:string` | 폴더 권한 핸들입니다. |
| hasSubfolder | `types:Boolean` | 폴더에 하위 폴더가 있는지 확인합니다. |
| subfolderArray | `types:FolderArray` | 폴더의 하위 폴더 배열입니다. |
