---
description: 작업 로그 정보.
solution: Experience Manager
title: 작업 로그 세부 사항
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fe41a48a-4671-4179-a128-aadc7bc0683b
TQID: 'https://experienceleague.adobe.com/wH0F5TxaTHxn-vP7PTri94WxEa5Bs9Q2-CRnuHdVb3I'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 60
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

