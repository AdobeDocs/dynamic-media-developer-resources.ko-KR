---
description: 이미지 자산과 연결된 이미지 필드를 업데이트합니다.
solution: Experience Manager
title: ImageFieldUpdate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82bc016b-8a2b-4811-a0b4-1e2a93add3b6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 11%

---

# ImageFieldUpdate{#imagefieldupdate}

이미지 자산과 연결된 이미지 필드를 업데이트합니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| assetHandle | `xsd:string` | 자산 핸들. |
| 해상도 | `xsd:double` | 인치당 이미지 해상도(픽셀 단위)입니다. |
| anchorX | `xsd:int` | X축 이미지 앵커. |
| anchorY | `xsd:int` | Y축 이미지 앵커. |
| 사용자 데이터 | `xsd:string` | 값 `userData` 이미지 제공 사용자 데이터 카탈로그 필드에 게시되는 메타데이터 필드입니다. |
