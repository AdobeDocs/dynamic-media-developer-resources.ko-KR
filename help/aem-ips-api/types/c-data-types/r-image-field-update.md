---
description: 이미지 자산과 연결된 이미지 필드를 업데이트합니다.
solution: Experience Manager
title: 이미지 필드 업데이트
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82bc016b-8a2b-4811-a0b4-1e2a93add3b6
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '56'
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
