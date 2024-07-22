---
title: init
description: 인라인 확대/축소 뷰어에 대한 JavaScript API 참조입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: c4419728-1e1a-4e11-88fe-24eb0c968c5c
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---

# init{#init}

인라인 확대/축소 뷰어에 대한 JavaScript API 참조입니다.

`init()`

뷰어 코드가 해당 ID로 찾을 수 있도록 뷰어의 초기화를 시작합니다. 이 시점까지 컨테이너 DOM 요소를 만들어야 합니다.

컨테이너 요소가 아직 웹 페이지 레이아웃의 일부가 아닌 경우(예: 할당된 `display:none` 스타일을 사용하여 숨길 수 있음) 뷰어가 초기화 프로세스를 일시 중단합니다. 웹 페이지가 컨테이너 요소를 레이아웃으로 다시 가져오는 순간까지 그렇게 됩니다. 이 작업이 발생하면 뷰어 로드가 자동으로 다시 시작됩니다.

뷰어 라이프사이클 중에 이 메서드를 한 번만 호출하면 됩니다. 이후의 호출은 무시됩니다.

## 매개 변수 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

없음.

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 뷰어 인스턴스에 대한 참조입니다.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
