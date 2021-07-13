---
description: 대화형 비디오 뷰어는 뷰어에 구성 매개 변수로 전달된 대화형 데이터를 기반으로 대화형 색상 견본 렌더링을 지원합니다.
solution: Experience Manager
title: 대화형 데이터 지원
feature: Dynamic Media Classic,Viewers,SDK/API,대화형 비디오
role: Developer,User
exl-id: 9118bf02-16ae-4dab-92e4-17347e866cc9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 0%

---

# 대화형 데이터 지원{#interactive-data-support}

대화형 비디오 뷰어는 뷰어에 구성 매개 변수로 전달된 대화형 데이터를 기반으로 대화형 색상 견본 렌더링을 지원합니다.

현재 표시된 견본은 연결된 비디오 시간 영역에 해당합니다. 대화형 색상 견본을 클릭하거나 탭하면 작성 시에 지정된 작업이 트리거됩니다.

대화형 색상 견본은 JavaScript 콜백을 트리거하여 호스팅 웹 페이지에서 빠른 보기를 활성화하거나 사용자를 외부 웹 페이지로 리디렉션할 수 있습니다.

## 빠른 보기 정보 {#section-7990e44f641042d2a38ba20c9413b3f8}

이러한 유형의 대화형 색상 견본은 AEM Assets의 작업 유형 &quot;quickview&quot;를 사용하여 작성해야 합니다. 사용자가 이러한 색상 견본을 활성화하면 뷰어는 `quickViewActivate` JavaScript 콜백을 실행하고 견본 데이터를 이 견본에 전달합니다. 포함 웹 페이지가 이 콜백을 수신하고 트리거될 때 페이지가 고유한 빠른 보기 구현을 열어야 합니다.

## 외부 웹 페이지로 리디렉션 {#section-32ebe3c3a7f74892a428c5d48801de4d}

AEM Assets에서 작업 유형 &quot;quickview&quot;에 대해 작성된 색상 견본 - 온디맨드 방식으로 사용자를 외부 URL로 리디렉션합니다. 작성 시의 설정에 따라 URL은 새 브라우저 탭, 동일한 창 또는 명명된 브라우저 창에서 열 수 있습니다.
