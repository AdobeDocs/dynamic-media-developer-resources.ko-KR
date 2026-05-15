---
description: 이 릴리스(이미지 제공 6.6.1 및 이미지 렌더링 6.6.1)는 이미지 제공 6.5.3 및 이미지 렌더링 6.5.3보다 우선합니다.
solution: Experience Manager
title: 이 릴리스 정보
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f837191b-1151-4c29-8059-b4d3e09e304e
TQID: 'https://experienceleague.adobe.com/Mv84kHB7jsBYAvY1j--l8Ly5VZtKwFq-SsNdz2TIQOE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 130
ht-degree: 1%

---

# 이 릴리스 정보{#about-this-release}

이 릴리스(이미지 제공 6.6.1 및 이미지 렌더링 6.6.1)는 이미지 제공 6.5.3 및 이미지 렌더링 6.5.3보다 우선합니다.

## 알려진 문제 및 동작 변경 {#section-9dbc05206187477f926a78e8108a34e1}

* 문자가 URL로 인코딩되어 있더라도 자산 ID의 물음표 문자는 더 이상 지원되지 않습니다.
* 동적 배너 `/xfl/flash/` 요청이 더 이상 지원되지 않으며 이제 HTTP 404 오류 코드를 반환합니다.
* W2P `/is/agm/` 요청은 더 이상 지원되지 않습니다.
* 일부 오류 메시지는 더 이상 브라우저에 렌더링되지 않습니다. 따라서 디버그할 추적 로그를 검토해야 합니다.

## 새로운 기능 {#section-b1386e36cb4544ebb79766a06b16842d}

* 스마트 견본
* 스마트 자르기

## 버그 수정 {#section-58dff74d56f64edeadf8f8b97b7a4161}

* `\qc` RTF 옵션 뒤에 공백이 있으면 요청이 렌더링되지 않는 문제가 해결되었습니다.
