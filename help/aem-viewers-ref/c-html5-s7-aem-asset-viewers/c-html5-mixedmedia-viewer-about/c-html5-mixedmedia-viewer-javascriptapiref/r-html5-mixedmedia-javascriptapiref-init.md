---
title: init
description: 혼합 미디어 뷰어에 대한 JavaScript API 참조.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 4fb40cec-172a-41b3-98fc-927da88c7cb9
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 2%

---

# init{#init}

혼합 미디어 뷰어에 대한 JavaScript API 참조.

`init()`

혼합 미디어 뷰어의 초기화를 시작합니다. 이 시점에는 뷰어 코드가 ID로 찾을 수 있도록 컨테이너 DOM 요소를 만들어야 합니다.

컨테이너 요소가 아직 웹 페이지 레이아웃의 일부가 아닌 경우(예: `display:none` style - 뷰어는 초기화 프로세스를 일시 중지합니다. 웹 페이지가 컨테이너 요소를 레이아웃으로 다시 가져올 때까지 일시 중단되며 이때 뷰어 로드가 자동으로 다시 시작됩니다.

뷰어 수명 주기 동안 이 메서드를 한 번만 호출합니다. 후속 호출은 무시됩니다.

## 매개 변수 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

없음.

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 뷰어 인스턴스에 대한 참조.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
