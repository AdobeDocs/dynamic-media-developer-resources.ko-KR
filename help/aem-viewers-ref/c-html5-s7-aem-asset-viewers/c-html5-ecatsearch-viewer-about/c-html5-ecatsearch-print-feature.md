---
description: 뷰어에서는 카탈로그 컨텐츠를 프린터로 출력할 수 있습니다.
solution: Experience Manager
title: 인쇄 기능
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog 검색
role: Developer,User
exl-id: eadcc105-4a86-40f7-867a-3b09a5599a41
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# 인쇄 기능{#print-feature}

뷰어에서는 카탈로그 컨텐츠를 프린터로 출력할 수 있습니다.

인쇄 기능은 도구 모음의 전용 단추에 의해 트리거됩니다. 버튼을 클릭하면 사용자가 인쇄 범위와 시트당 페이지 수를 선택할 수 있습니다.

인쇄 품질은 `printquality` 구성 매개 변수를 사용하여 조정할 수 있습니다. `printquality` 을 기본값보다 크게 높은 값으로 설정하면 안 됩니다. 그 이유는 클라이언트 시스템의 웹 브라우저에 의해 메모리 사용량이 매우 많기 때문입니다. 또한 Dynamic Media Classic 회사에 대해 설정된 최대 이미지 응답 크기가 구성된 `printquality` 값보다 커야 합니다.

>[!NOTE]
>
>인쇄 기능은 Internet Explorer 9를 제외한 데스크톱 시스템에서만 사용할 수 있습니다.
