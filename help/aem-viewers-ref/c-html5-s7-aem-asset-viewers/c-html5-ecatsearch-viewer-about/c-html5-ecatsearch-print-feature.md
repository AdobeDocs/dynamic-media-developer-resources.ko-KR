---
description: 뷰어를 사용하면 카탈로그 내용을 프린터로 출력할 수 있습니다.
solution: Experience Manager
title: 인쇄 기능
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: eadcc105-4a86-40f7-867a-3b09a5599a41
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 0%

---

# 인쇄 기능{#print-feature}

뷰어를 사용하면 카탈로그 내용을 프린터로 출력할 수 있습니다.

인쇄 기능은 도구 모음의 전용 버튼에 의해 트리거됩니다. 버튼을 클릭하면 사용자가 인쇄 범위와 한 면에 대한 페이지 수를 선택할 수 있습니다.

인쇄 품질은 다음을 사용하여 조정할 수 있습니다 `printquality` 구성 매개 변수. 이 설정에 유의하십시오. `printquality` 기본값보다 상당히 높은 값은 사용하지 않는 것이 좋습니다. 그 이유는 클라이언트 시스템의 웹 브라우저에 의한 매우 높은 메모리 소비로 이어지기 때문이다. 또한 Dynamic Media Classic 회사에 대해 설정된 최대 이미지 응답 크기가 구성된 크기보다 큰지 확인하십시오 `printquality` 값.

>[!NOTE]
>
>인쇄 기능은 Internet Explorer 9를 제외한 데스크탑 시스템에서만 사용할 수 있습니다.
