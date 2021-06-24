---
description: 이 릴리스는 Image Serving 6.6.1과 Image Rendering 6.6.1이 Image Serving 6.5.3과 Image Rendering 6.5.3보다 우선합니다.
solution: Experience Manager
title: 이 릴리스 노트
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: f837191b-1151-4c29-8059-b4d3e09e304e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 1%

---

# 이 릴리스 노트{#about-this-release}

이 릴리스는 Image Serving 6.6.1과 Image Rendering 6.6.1이 Image Serving 6.5.3과 Image Rendering 6.5.3보다 우선합니다.

## 알려진 문제 및 동작 변경 사항 {#section-9dbc05206187477f926a78e8108a34e1}

* 문자가 URL로 인코딩되어 있더라도 자산 ID에서 물음표 문자를 더 이상 사용할 수 없습니다.
* 동적 배너 `/xfl/flash/` 요청은 더 이상 지원되지 않으며 이제 http 404 오류 코드를 반환합니다.
* W2P `/is/agm/` 요청은 더 이상 지원되지 않습니다.
* 일부 오류 메시지가 더 이상 브라우저에 렌더링되지 않습니다. 따라서 디버그하려면 추적 로그를 검토해야 합니다.

## 새로운 기능 {#section-b1386e36cb4544ebb79766a06b16842d}

* 스마트 견본
* 스마트 자르기

## 버그 수정 {#section-58dff74d56f64edeadf8f8b97b7a4161}

* `\qc` RTF 옵션 다음에 공백이 오는 경우 요청이 렌더링되지 않는 문제가 해결되었습니다.
