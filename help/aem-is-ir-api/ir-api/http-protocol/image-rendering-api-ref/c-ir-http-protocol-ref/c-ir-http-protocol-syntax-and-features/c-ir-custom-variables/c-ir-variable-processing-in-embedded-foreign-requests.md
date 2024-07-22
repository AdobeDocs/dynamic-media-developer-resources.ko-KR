---
title: 포함된 외부 요청에서 변수 처리
description: 포함된 외래 요청의 중괄호 안에 있는 모든 위치에서 발생하는 $var$ 참조는 일치하는 변수 정의 값으로 대체됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a87bb2a0-0554-4978-982d-b6617925cd53
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# 포함된 외부 요청에서 변수 처리{#variable-processing-in-embedded-foreign-requests}

포함된 외부 요청의 중괄호 안에 있는 모든 `$var$` 참조는 일치하는 변수 정의 값으로 대체됩니다.

이미지 카탈로그의 템플릿에 임베드된 외부 요청을 배치할 수 있습니다.

서버가 최종 외부 URL을 전송하려고 시도하기 전에 다시 인코딩이 적용되지 않으므로 외부 요청으로 대체되는 변수 값은 일반적으로 이중 인코딩이 적용되어야 합니다.
