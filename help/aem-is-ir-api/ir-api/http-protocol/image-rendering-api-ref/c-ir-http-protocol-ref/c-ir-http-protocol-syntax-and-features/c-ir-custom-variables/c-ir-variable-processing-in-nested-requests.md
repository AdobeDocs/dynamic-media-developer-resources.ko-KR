---
title: 중첩 요청의 변수 처리
description: $var$ 참조는 '?' 왼쪽의 를 포함하여 중첩된 이미지 제공 또는 이미지 렌더링 요청의 중괄호 내의 어디에서든 발생할 수 있습니다. 쿼리에서 경로 구분
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa82ec48-aeec-4cd9-8d2e-cf9c913c67a7
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# 중첩 요청의 변수 처리{#variable-processing-in-nested-requests}

$var$ 참조는 &#39;?&#39; 왼쪽의 를 포함하여 중첩된 이미지 제공 또는 이미지 렌더링 요청의 중괄호 내의 어디에서든 발생할 수 있습니다. 쿼리에서 경로 구분

서버는 이러한 참조를 URL의 값 또는 `catalog::Modifier` 중첩된 요청의 추가 구문 분석 및 처리 전에 기본 이미지 카탈로그의 매개 변수를 검토하십시오.

게다가, `$ *[!DNL var]*=` url 및 의 정의 `catalog::Modifier` 모든 중첩 이미지 제공 및 이미지 렌더링 요청으로 전달됩니다. 이렇게 하면 중첩 수준에 관계없이 모든 템플릿에서 모든 변수 정의를 사용할 수 있습니다.

중첩 수준에 관계없이, 중첩 이미지 렌더링 또는 이미지 제공 요청의 어느 곳에서든 대체될 변수 값에는 단일 패스 HTTP 인코딩만 적용되어야 합니다.
