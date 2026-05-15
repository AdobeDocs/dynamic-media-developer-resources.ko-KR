---
description: 이미지 자산과 연결된 이미지 필드를 업데이트합니다.
solution: Experience Manager
title: 이미지 필드 업데이트
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82bc016b-8a2b-4811-a0b4-1e2a93add3b6
TQID: 'https://experienceleague.adobe.com/IsOZvDzvJTa0KJfUkYblEln9Qrx7nQm79FEEbnFVjiw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 56
ht-degree: 8%

---

# [!DNL ImageFieldUpdate]{#imagefieldupdate}

이미지 자산과 연결된 이미지 필드를 업데이트합니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| assetHandle | `xsd:string` | 에셋 핸들. |
| [!DNL resolution] | `xsd:double` | 인치당 픽셀 단위의 이미지 해상도. |
| [!DNL anchorX] | `xsd:int` | X축 이미지 앵커입니다. |
| [!DNL anchorY] | `xsd:int` | Y축 이미지 앵커입니다. |
| [!DNL userData] | `xsd:string` | 이미지 제공 사용자 데이터 카탈로그 필드에 게시된 `userData` 메타데이터 필드의 값입니다. |
