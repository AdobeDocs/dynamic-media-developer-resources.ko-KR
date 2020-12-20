---
description: 스핀 뷰어용 JavaScript API 참조입니다.
seo-description: 스핀 뷰어용 JavaScript API 참조입니다.
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic media
uuid: 1803028f-dcba-49da-9fb7-78bfd64fc47d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---


# init{#init}

스핀 뷰어용 JavaScript API 참조입니다.

`init()`

스핀 뷰어의 초기화를 시작합니다. 이때 뷰어 코드가 ID로 이를 찾을 수 있도록 `DOM` 컨테이너를 만들어야 합니다.

컨테이너 요소가 웹 페이지 레이아웃의 일부가 아닌 경우(예: 여기에 할당된 `display:none` 스타일을 사용하여 숨겨질 수 있음), 뷰어는 웹 페이지가 컨테이너 요소를 레이아웃으로 다시 가져올 때까지 초기화 프로세스를 일시 중단합니다. 이 경우 뷰어 부하가 자동으로 다시 시작됩니다.

이 메서드는 뷰어 수명 주기 동안 한 번만 호출합니다.후속 호출은 무시됩니다.

## 매개 변수 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

없음.

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101} 반환

`{Object}` 뷰어 인스턴스에 대한 참조입니다.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

