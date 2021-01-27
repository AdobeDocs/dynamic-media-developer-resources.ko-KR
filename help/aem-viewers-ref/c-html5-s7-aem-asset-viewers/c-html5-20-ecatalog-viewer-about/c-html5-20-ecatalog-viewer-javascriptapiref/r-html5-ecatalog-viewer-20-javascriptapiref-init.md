---
description: eCatalog 뷰어에 대한 JavaScript API 참조 사항입니다.
seo-description: eCatalog 뷰어에 대한 JavaScript API 참조 사항입니다.
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic Media
uuid: 142381e4-aa3c-46dd-a0bd-4e090d0003e4
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---


# init{#init}

eCatalog 뷰어에 대한 JavaScript API 참조 사항입니다.

`init()`

eCatalog 뷰어의 초기화를 시작합니다. 이 시점에는 뷰어 코드가 ID로 이를 찾을 수 있도록 컨테이너 DOM 요소를 만들어야 합니다.

컨테이너 요소가 웹 페이지 레이아웃의 일부가 아닌 경우(예: 여기에 할당된 `display:none` 스타일을 사용하여 숨겨질 수 있음), 뷰어는 웹 페이지가 컨테이너 요소를 레이아웃으로 다시 가져올 때까지 초기화 프로세스를 일시 중단합니다. 이 경우 뷰어 로드가 자동으로 다시 시작됩니다.

뷰어 수명 주기 동안 이 메서드를 한 번만 호출합니다.후속 호출은 무시됩니다.

## 매개 변수 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

없음.

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101} 반환

`{Object}` 뷰어 인스턴스에 대한 참조입니다.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
\<instance>.init()
```

