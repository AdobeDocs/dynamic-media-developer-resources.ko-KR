---
description: 계층 파일 또는 자산 저장소 개체. 폴더에는 하나 이상의 하위 폴더가 포함될 수 있습니다.
solution: Experience Manager
title: 폴더
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 74b44b1a-a92e-4c97-a93b-0cd4552f78ec
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 10%

---

# 폴더{#folder}

계층 파일 또는 자산 저장소 개체. 폴더에는 하나 이상의 하위 폴더가 포함될 수 있습니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| `*`folderHandle`*` | `xsd:string` | 폴더 핸들. |
| `*`경로`*` | `xsd:string` | 폴더 경로. |
| `*`lastModified`*` | `xsd:dateTime` | 마지막 수정 날짜. |
| `*`childLastModified`*` | `xsd:dateTime` | 하위 폴더 및 폴더 하위 자산에 대한 마지막 수정 날짜입니다. |
| `*`permissionsSetHandle`*` | `xsd:string` | 폴더 권한 핸들입니다. |
| `*`hasSubfolder`*` | `types:Boolean` | 폴더에 하위 폴더가 있는지 확인합니다. |
| `*`subfolderArray`*` | `types:FolderArray` | 폴더의 하위 폴더 배열입니다. |
