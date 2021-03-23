---
description: 뷰어를 사용하면 카탈로그 내용을 프린터로 출력할 수 있습니다.
seo-description: 뷰어를 사용하면 카탈로그 내용을 프린터로 출력할 수 있습니다.
seo-title: 인쇄 기능
solution: Experience Manager
title: 인쇄 기능
uuid: 4932042a-1421-4589-8bf5-88bbe38d774d
feature: Dynamic Media Classic,뷰어,SDK/API,eCatalog 검색
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---


# 인쇄 기능{#print-feature}

뷰어를 사용하면 카탈로그 내용을 프린터로 출력할 수 있습니다.

인쇄 기능은 도구 모음의 전용 단추에 의해 트리거됩니다. 이 단추를 클릭하면 인쇄 범위와 시트당 페이지 수를 선택할 수 있습니다.

인쇄 품질은 `printquality` 구성 매개 변수를 사용하여 조정할 수 있습니다. `printquality`을 기본값보다 크게 높은 값으로 설정하는 것은 권장되지 않습니다. 그 이유는 클라이언트 시스템의 웹 브라우저에 의한 메모리 사용량이 매우 높기 때문입니다. 또한 Dynamic Media Classic 회사에 대해 설정된 최대 이미지 응답 크기가 구성된 `printquality` 값보다 큰지 확인하십시오.

>[!NOTE]
>
>인쇄 기능은 Internet Explorer 9를 제외한 데스크탑 시스템에서만 사용할 수 있습니다.

