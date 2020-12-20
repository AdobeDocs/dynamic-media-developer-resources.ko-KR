---
description: 포함된 외래 요청의 중괄호 내에서 발생하는 $var$ 참조는 일치하는 변수 정의 값으로 대체됩니다.
seo-description: 포함된 외래 요청의 중괄호 내에서 발생하는 $var$ 참조는 일치하는 변수 정의 값으로 대체됩니다.
seo-title: 임베디드 외부 요청의 변수 처리
solution: Experience Manager
title: 임베디드 외부 요청의 변수 처리
topic: Scene7 Image Serving - Image Rendering API
uuid: b4334a2e-dab1-4458-ab3d-bb79d2c4fdd4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---


# 포함된 외부 요청의 변수 처리{#variable-processing-in-embedded-foreign-requests}

포함된 외래 요청의 중괄호 내에서 발생하는 $var$ 참조는 일치하는 변수 정의 값으로 대체됩니다.

이를 통해 임베드된 외부 요청을 이미지 카탈로그의 템플릿에 배치할 수 있습니다.

서버가 최종 외래 URL을 전송하려고 시도하기 전에 다시 인코딩이 적용되지 않으므로 일반적으로 외부 요청으로 대체될 변수 값은 이중 인코딩되어야 합니다.
