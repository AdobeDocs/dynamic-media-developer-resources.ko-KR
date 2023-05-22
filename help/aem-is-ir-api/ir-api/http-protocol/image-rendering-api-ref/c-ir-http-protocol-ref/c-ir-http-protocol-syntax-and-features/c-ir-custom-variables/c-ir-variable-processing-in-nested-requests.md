---
title: 중첩된 요청에서 변수 처리
description: $var$ 참조는 '?' 왼쪽을 포함하여 중첩된 이미지 제공 또는 이미지 렌더링 요청의 중괄호 내 아무 곳에서나 발생할 수 있습니다. 쿼리에서 경로 구분.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa82ec48-aeec-4cd9-8d2e-cf9c913c67a7
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# 중첩된 요청에서 변수 처리{#variable-processing-in-nested-requests}

$var$ 참조는 &#39;?&#39; 왼쪽을 포함하여 중첩된 이미지 제공 또는 이미지 렌더링 요청의 중괄호 내 아무 곳에서나 발생할 수 있습니다. 쿼리에서 경로 구분.

서버는 이러한 참조를 다음 값(url 또는 `catalog::Modifier` 중첩된 요청의 추가 구문 분석 및 처리 전 기본 이미지 카탈로그의 참조).

또한, 모두 `$ *[!DNL var]*=` url 및 `catalog::Modifier` 모든 중첩 이미지 제공 및 이미지 렌더링 요청으로 전달됩니다. 이렇게 하면 중첩 수준에 관계없이 모든 템플릿에서 모든 변수 정의를 사용할 수 있습니다.

중첩 수준에 관계없이, 중첩된 이미지 렌더링 또는 이미지 제공 요청의 모든 위치에서 대체할 변수 값에는 단일 패스 HTTP 인코딩만 적용해야 합니다.
