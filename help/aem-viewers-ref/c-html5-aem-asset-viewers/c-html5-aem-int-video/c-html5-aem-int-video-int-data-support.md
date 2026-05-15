---
title: 대화형 데이터 지원
description: 대화형 비디오 뷰어는 뷰어에 구성 매개 변수로 전달된 대화형 데이터를 기반으로 대화형 견본 렌더링을 지원합니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 9118bf02-16ae-4dab-92e4-17347e866cc9
TQID: 'https://experienceleague.adobe.com/HE4LeluT9FWi8xgQf259b1yakK0oQjeR3rDME0juZiU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 223
ht-degree: 0%

---

# 대화형 데이터 지원{#interactive-data-support}

대화형 비디오 뷰어는 뷰어에 구성 매개 변수로 전달된 대화형 데이터를 기반으로 대화형 견본 렌더링을 지원합니다.

현재 표시되는 견본은 연결된 비디오 시간 영역에 해당합니다. 대화형 견본을 클릭하거나 탭하면 작성 시 견본에 할당된 작업이 트리거됩니다.

대화형 견본은 JavaScript 콜백을 트리거하여 호스팅 웹 페이지에서 빠른 보기를 활성화하거나 사용자를 외부 웹 페이지로 리디렉션할 수 있습니다.

## 빠른 보기 정보 {#section-7990e44f641042d2a38ba20c9413b3f8}

이러한 유형의 대화형 견본은 Adobe Experience Manager Assets - On-demand의 &quot;빠른 보기&quot; 작업 유형을 사용하여 작성해야 합니다. 사용자가 이러한 견본을 활성화하면 뷰어가 `quickViewActivate` JavaScript 콜백을 실행하고 견본 데이터를 전달합니다. 포함 웹 페이지가 이 콜백을 수신하고 트리거할 때 페이지가 자체 Quickview 구현을 여는 것으로 예상됩니다.

## 외부 웹 페이지로 리디렉션 {#section-32ebe3c3a7f74892a428c5d48801de4d}

Experience Manager Assets에서 작업 유형 &quot;빠른 보기&quot;에 대해 작성된 견본 - 온디맨드로 사용자를 외부 URL로 리디렉션합니다. 작성 시의 설정에 따라 URL은 새 브라우저 탭, 동일한 창 또는 명명된 브라우저 창에서 열 수 있습니다.
