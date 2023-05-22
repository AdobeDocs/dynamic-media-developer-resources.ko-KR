---
description: 작업 항목 진행 정보.
solution: Experience Manager
title: 작업 항목 진행률
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 568a5601-b928-447d-8297-01139f36cf73
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '32'
ht-degree: 18%

---

# [!DNL TaskItemProgress]{#taskitemprogress}

작업 항목 진행 정보.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| itemName | `xsd:string` | 처리 중인 항목의 이름입니다. |
| progress | `xsd:double` | 진행률 완료 % |
| progressMessage | `xsd:string` | 메시지 처리. |
| lastProgressUpdate | `xsd:dateTime` | 마지막 업데이트 시간. |
