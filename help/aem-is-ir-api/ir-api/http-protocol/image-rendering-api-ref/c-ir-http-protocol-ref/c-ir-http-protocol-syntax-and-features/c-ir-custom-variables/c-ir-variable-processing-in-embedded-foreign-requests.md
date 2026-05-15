---
title: 포함된 외부 요청에서 변수 처리
description: 포함된 외래 요청의 중괄호 안에 있는 모든 위치에서 발생하는 $var$ 참조는 일치하는 변수 정의 값으로 대체됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a87bb2a0-0554-4978-982d-b6617925cd53
TQID: 'https://experienceleague.adobe.com/-0KT9d6qz9-8d41vKNgbCYUKQQLBRaLE-0TFmyIvRCM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 98
ht-degree: 0%

---

# 포함된 외부 요청에서 변수 처리{#variable-processing-in-embedded-foreign-requests}

포함된 외부 요청의 중괄호 안에 있는 모든 `$var$` 참조는 일치하는 변수 정의 값으로 대체됩니다.

이미지 카탈로그의 템플릿에 임베드된 외부 요청을 배치할 수 있습니다.

서버가 최종 외부 URL을 전송하려고 시도하기 전에 다시 인코딩이 적용되지 않으므로 외부 요청으로 대체되는 변수 값은 일반적으로 이중 인코딩이 적용되어야 합니다.
