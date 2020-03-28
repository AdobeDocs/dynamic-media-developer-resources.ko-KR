---
description: $var$ 참조는 '?'의 왼쪽에 포함하여 중첩된 이미지 제공 또는 이미지 렌더링 요청의 중괄호 내에서 발생할 수 있습니다. 쿼리와 경로 구분
seo-description: $var$ 참조는 '?'의 왼쪽에 포함하여 중첩된 이미지 제공 또는 이미지 렌더링 요청의 중괄호 내에서 발생할 수 있습니다. 쿼리와 경로 구분
seo-title: 중첩된 요청의 변수 처리
solution: Experience Manager
title: 중첩된 요청의 변수 처리
topic: Scene7 Image Serving - Image Rendering API
uuid: 2f3fefac-d45e-4c53-854f-1fe16d0cedd9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 중첩된 요청의 변수 처리{#variable-processing-in-nested-requests}

$var$ 참조는 &#39;?&#39;의 왼쪽에 포함하여 중첩된 이미지 제공 또는 이미지 렌더링 요청의 중괄호 내에서 발생할 수 있습니다. 쿼리와 경로 구분

서버는 중첩된 요청의 추가 구문 분석 및 처리를 수행하기 전에 이러한 참조를 URL 또는 기본 이미지 카탈로그의 값으로 `catalog::Modifier` 대체합니다.

또한 URL의 모든 `$ *[!DNL var]*=` 정의가 중첩된 모든 이미지 제공 및 이미지 렌더링 요청으로 `catalog::Modifier` 전달됩니다. 이렇게 하면 중첩 수준에 관계없이 모든 템플릿에서 모든 변수 정의를 사용할 수 있습니다.

중첩 수준에 관계없이, 단일 통과 HTTP 인코딩만 중첩된 이미지 렌더링 또는 이미지 제공 요청의 어느 곳에서나 대체할 변수 값에 적용되어야 합니다.
