---
description: 작업 로그 정보.
solution: Experience Manager
title: 작업 로그 세부 사항
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fe41a48a-4671-4179-a128-aadc7bc0683b
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 8%

---

# [!DNL JobLogDetail]{#joblogdetail}

작업 로그 정보.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| logMessage | `xsd:string` | 작업 로그의 메시지. |
| logType | `xsd:string` | 작업 로그 파일 유형. |
| assetName | `xsd:string` | 작업 로그의 에셋 이름(선택 사항). |
| assetType | `xsd:string` | 에셋 유형 선택. |
| assetHandle | `xsd:string` | 작업 로그에서 참조된 자산 핸들. |
| auxArray | `types:JobLogDetailAuxArray` | 위에서 설명한 5가지 작업 로그 유형 이외의 자세한 작업 로그 정보를 제공합니다. |
