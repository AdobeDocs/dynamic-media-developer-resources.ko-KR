---
description: 이미지 자산과 연관된 이미지 필드를 업데이트합니다.
solution: Experience Manager
title: ImageFieldUpdate
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 8%

---


# ImageFieldUpdate{#imagefieldupdate}

이미지 자산과 연관된 이미지 필드를 업데이트합니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 자산 핸들. |
| `*`resolution`*` | `xsd:double` | 이미지 해상도(인치당 픽셀 단위) |
| `*`anchorX`*` | `xsd:int` | X축 이미지 앵커. |
| `*`anchorY`*` | `xsd:int` | Y축 이미지 앵커. |
| `*`사용자 데이터`*` | `xsd:string` | `userData` 메타데이터 필드의 값입니다. 이 필드는 이미지 제공 사용자 데이터 카탈로그 필드에 게시됩니다. |

