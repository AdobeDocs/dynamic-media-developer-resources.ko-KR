---
description: This release—Image Serving 6.6.1 and Image Rendering 6.6.1은 Image Serving 6.5.3 and Image Rendering 6.5.3보다 우선합니다.
seo-description: This release—Image Serving 6.6.1 and Image Rendering 6.6.1은 Image Serving 6.5.3 and Image Rendering 6.5.3보다 우선합니다.
seo-title: 이 릴리스 정보
solution: Experience Manager
title: 이 릴리스 정보
topic: Scene7 Image Serving - Image Rendering API
uuid: 2fdd8920-433b-405e-bf93-dbef5735be3f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 이 릴리스 정보{#about-this-release}

This release—Image Serving 6.6.1 and Image Rendering 6.6.1은 Image Serving 6.5.3 and Image Rendering 6.5.3보다 우선합니다.

## 알려진 문제 및 동작 변경 사항 {#section-9dbc05206187477f926a78e8108a34e1}

* 문자가 URL로 인코딩된 경우에도 자산 ID에서 물음표 문자 사용이 더 이상 지원되지 않습니다.
* 동적 배너 `/xfl/flash/` 요청은 더 이상 지원되지 않으며 이제 http 404 오류 코드를 반환합니다.
* W2P `/is/agm/` 요청은 더 이상 지원되지 않습니다.
* 일부 오류 메시지가 더 이상 브라우저로 렌더링되지 않습니다. 따라서 추적 로그를 검토하여 디버깅해야 합니다.

## 새로운 기능 {#section-b1386e36cb4544ebb79766a06b16842d}

* 스마트 견본
* 스마트 자르기

## 버그 수정 {#section-58dff74d56f64edeadf8f8b97b7a4161}

* RTF 옵션 다음에 `\qc` 공백이 오는 경우 요청이 렌더링되지 않는 문제가 해결되었습니다.

