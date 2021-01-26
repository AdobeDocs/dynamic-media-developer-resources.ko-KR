---
description: 이 릴리스(Image Serving 6.6.1 및 Image Rendering 6.6.1)은 Image Serving 6.5.3 및 Image Rendering을 대체합니다. 6.5.3.
seo-description: 이 릴리스(Image Serving 6.6.1 및 Image Rendering 6.6.1)은 Image Serving 6.5.3 및 Image Rendering을 대체합니다. 6.5.3.
seo-title: 이 릴리스 정보
solution: Experience Manager
title: 이 릴리스 정보
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 2fdd8920-433b-405e-bf93-dbef5735be3f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 1%

---


# 이 릴리스 정보{#about-this-release}

이 릴리스(Image Serving 6.6.1 및 Image Rendering 6.6.1)은 Image Serving 6.5.3 및 Image Rendering을 대체합니다. 6.5.3.

## 알려진 문제 및 비헤이비어 변경 사항 {#section-9dbc05206187477f926a78e8108a34e1}

* 문자가 URL로 인코딩된 경우에도 자산 ID에서 물음표 문자 사용이 더 이상 지원되지 않습니다.
* 동적 배너 `/xfl/flash/` 요청은 더 이상 지원되지 않으며 이제 http 404 오류 코드를 반환합니다.
* W2P `/is/agm/` 요청은 더 이상 지원되지 않습니다.
* 일부 오류 메시지가 더 이상 브라우저로 렌더링되지 않습니다. 따라서 디버깅하려면 추적 로그를 검토해야 합니다.

## 새로운 기능 {#section-b1386e36cb4544ebb79766a06b16842d}

* 스마트 견본
* 스마트 자르기

## 버그 수정 {#section-58dff74d56f64edeadf8f8b97b7a4161}

* `\qc` RTF 옵션 다음에 공백이 오는 경우 요청이 렌더링되지 않는 문제가 해결되었습니다.

