---
description: 이 릴리스(이미지 제공 6.6.1 및 이미지 렌더링 6.6.1)는 이미지 제공 6.5.3 및 이미지 렌더링 6.5.3보다 우선합니다.
solution: Experience Manager
title: 이 릴리스 정보
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f837191b-1151-4c29-8059-b4d3e09e304e
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 1%

---

# 이 릴리스 정보{#about-this-release}

이 릴리스(이미지 제공 6.6.1 및 이미지 렌더링 6.6.1)는 이미지 제공 6.5.3 및 이미지 렌더링 6.5.3보다 우선합니다.

## 알려진 문제 및 동작 변경 {#section-9dbc05206187477f926a78e8108a34e1}

* 문자가 URL로 인코딩되어 있더라도 자산 ID의 물음표 문자는 더 이상 지원되지 않습니다.
* 동적 배너 `/xfl/flash/` 요청은 더 이상 지원되지 않으며 이제 HTTP 404 오류 코드를 반환합니다.
* W2P `/is/agm/` 요청은 더 이상 지원되지 않습니다.
* 일부 오류 메시지는 더 이상 브라우저에 렌더링되지 않습니다. 따라서 디버그할 추적 로그를 검토해야 합니다.

## 새로운 기능 {#section-b1386e36cb4544ebb79766a06b16842d}

* 스마트 견본
* 스마트 자르기

## 버그 수정 {#section-58dff74d56f64edeadf8f8b97b7a4161}

* 이(가) 발생하는 문제가 해결되었습니다. `\qc` RTF 옵션 뒤에 공백이 있으면 요청이 렌더링되지 않습니다.
