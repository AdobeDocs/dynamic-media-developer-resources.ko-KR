---
description: 대화형 비디오 뷰어에 대한 JavaScript API 참조.
solution: Experience Manager
title: init
feature: Dynamic Media Classic,Viewers,SDK/API,대화형 비디오
role: Developer,User
exl-id: 5fcc7dcd-a9a8-4a87-9c8d-42717ced8ae9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 2%

---

# init{#init}

대화형 비디오 뷰어에 대한 JavaScript API 참조.

`init()`

대화형 비디오 뷰어의 초기화를 시작합니다. 이 시점에는 뷰어 코드가 ID로 찾을 수 있도록 컨테이너 DOM 요소를 만들어야 합니다.

컨테이너 요소가 웹 페이지 레이아웃의 일부가 아닌 경우(예: 이 요소에 지정된 `display:none` 스타일을 사용하여 숨길 수 있음) 뷰어는 웹 페이지가 컨테이너 요소를 다시 레이아웃으로 가져오는 시점까지 초기화 프로세스를 일시 중지합니다. 이런 경우 뷰어 로드가 자동으로 다시 시작됩니다.

이 메서드는 뷰어 수명 주기 동안 한 번만 호출합니다. 후속 호출은 무시됩니다.

## 매개 변수 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

없음.

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 뷰어 인스턴스에 대한 참조.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
