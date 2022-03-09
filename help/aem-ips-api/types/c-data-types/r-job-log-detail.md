---
description: 작업 로그 정보입니다.
solution: Experience Manager
title: 작업 로그 세부 정보
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fe41a48a-4671-4179-a128-aadc7bc0683b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 8%

---

# 작업 로그 세부 정보{#joblogdetail}

작업 로그 정보입니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| logMessage | `xsd:string` | 작업 로그의 메시지입니다. |
| logType | `xsd:string` | 작업 로그 파일 유형입니다. |
| assetName | `xsd:string` | 작업 로그에 있는 자산의 이름입니다(선택 사항). |
| assetType | `xsd:string` | 자산 유형 선택. |
| assetHandle | `xsd:string` | 작업 로그에서 참조되는 자산 핸들. |
| auxArray | `types:JobLogDetailAuxArray` | 위에서 설명한 5가지 작업 로그 유형 이외의 추가 작업 로그 정보를 제공합니다. |
