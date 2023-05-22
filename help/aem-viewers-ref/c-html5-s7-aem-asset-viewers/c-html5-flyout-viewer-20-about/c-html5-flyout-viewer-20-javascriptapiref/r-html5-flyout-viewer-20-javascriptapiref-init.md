---
description: 플라이아웃 뷰어에 대한 JavaScript API 참조.
solution: Experience Manager
title: init
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: e86f8c0f-c130-43c5-8c3a-07c6bc49e2f7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 2%

---

# init{#init}

플라이아웃 뷰어에 대한 JavaScript API 참조.

`init()`

플라이아웃 뷰어의 초기화를 시작합니다. 이 시점까지 뷰어 코드가 해당 ID로 찾을 수 있도록 컨테이너 DOM 요소를 만들어야 합니다.

컨테이너 요소가 아직 웹 페이지 레이아웃의 일부가 아닌 경우(예: 를 사용하여 숨길 수 있음) `display:none` 스타일이 할당됨)되면 뷰어는 웹 페이지가 컨테이너 요소를 레이아웃으로 다시 가져오는 순간까지 초기화 프로세스를 일시 중단합니다. 이 경우 뷰어 로드는 자동으로 다시 시작됩니다.

이 메서드는 뷰어 라이프사이클 중에 한 번만 호출해야 하므로 결과 호출은 무시됩니다.

## 매개 변수 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

없음.

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 뷰어 인스턴스에 대한 참조입니다.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
