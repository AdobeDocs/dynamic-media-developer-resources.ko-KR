---
title: init
description: 스핀 뷰어에 대한 JavaScript API 참조.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 5217a02a-6092-4cb9-b4fb-f959cdc85a6e
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 2%

---

# init{#init}

스핀 뷰어에 대한 JavaScript API 참조.

`init()`

스핀 뷰어의 초기화를 시작합니다. 이번에는 컨테이너 `DOM` 뷰어 코드가 ID로 찾을 수 있도록 요소를 만들어야 합니다.

컨테이너 요소가 아직 웹 페이지 레이아웃의 일부가 아닌 경우(예: `display:none` style - 뷰어는 초기화 프로세스를 일시 중지합니다. 웹 페이지가 컨테이너 요소를 레이아웃으로 다시 가져올 때까지 일시 중단되며 이때 뷰어 로드가 자동으로 다시 시작됩니다.

이 메서드는 뷰어 수명 주기 동안 한 번만 호출합니다. 후속 호출은 무시됩니다.

## 매개 변수 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

없음.

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 뷰어 인스턴스에 대한 참조.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
