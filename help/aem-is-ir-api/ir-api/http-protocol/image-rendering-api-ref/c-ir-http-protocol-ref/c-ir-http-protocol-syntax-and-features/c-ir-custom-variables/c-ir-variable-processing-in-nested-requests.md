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

서버는 중첩 요청을 추가로 구문 분석하고 처리하기 전에 이러한 참조를 값(URL 또는 기본 이미지 카탈로그의 `catalog::Modifier`에서)으로 대체합니다.

또한 URL 및 `catalog::Modifier`의 모든 `$ *[!DNL var]*=` 정의가 모든 중첩 이미지 제공 및 이미지 렌더링 요청으로 전달됩니다. 이렇게 하면 중첩 수준에 관계없이 모든 템플릿에서 모든 변수 정의를 사용할 수 있습니다.

중첩 수준에 관계없이, 중첩된 이미지 렌더링 또는 이미지 제공 요청의 모든 위치에서 대체할 변수 값에는 단일 패스 HTTP 인코딩만 적용해야 합니다.
