---
description: 인라인 확대/축소 뷰어에 대한 JavaScript API 참조입니다.
seo-description: 인라인 확대/축소 뷰어에 대한 JavaScript API 참조입니다.
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic media
uuid: a3bd0cd1-e4cb-4b09-a78f-0958b55a79e4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# init{#init}

인라인 확대/축소 뷰어에 대한 JavaScript API 참조입니다.

`init()`

뷰어 코드가 ID로 찾을 수 있도록 뷰어의 초기화를 시작합니다. 이때 컨테이너 DOM 요소를 만들어야 합니다.

컨테이너 요소가 아직 웹 페이지 레이아웃의 일부가 아닌 경우(예: 지정된 `display:none` 스타일을 사용하여 숨겨질 수 있음) 뷰어는 웹 페이지가 컨테이너 요소를 레이아웃으로 다시 가져올 때까지 초기화 프로세스를 일시 중단합니다. 이 경우 뷰어 부하가 자동으로 다시 시작됩니다.

뷰어 수명 주기 동안 이 메서드를 한 번만 호출합니다.후속 호출은 무시됩니다.

## 매개 변수 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

없음.

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 뷰어 인스턴스에 대한 참조입니다.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

