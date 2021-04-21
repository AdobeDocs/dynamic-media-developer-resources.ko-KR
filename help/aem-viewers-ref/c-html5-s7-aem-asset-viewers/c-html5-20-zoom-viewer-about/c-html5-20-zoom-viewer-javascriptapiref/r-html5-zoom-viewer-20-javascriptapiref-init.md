---
description: 비디오 뷰어용 JavaScript API 참조.
solution: Experience Manager
title: init
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 2%

---


# init{#init}

비디오 뷰어용 JavaScript API 참조.

`init()`

비디오 뷰어의 초기화를 시작합니다. 이때 뷰어 코드가 해당 ID로 이를 찾을 수 있도록 컨테이너 DOM 요소를 만들어야 합니다.

컨테이너 요소가 웹 페이지 레이아웃의 일부가 아닌 경우(예: 컨테이너 요소에 할당된 `display:none` 스타일을 사용하여 숨겨질 수 있으므로 웹 페이지가 컨테이너 요소를 레이아웃으로 다시 가져올 때까지 뷰어는 초기화 프로세스를 일시 중단합니다. 이 경우 뷰어 로드가 자동으로 다시 시작됩니다.

이 메서드는 뷰어 수명 주기 동안 한 번만 호출합니다.후속 호출은 무시됩니다.

## 매개 변수 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

없음.

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101} 반환

`{Object}` 뷰어 인스턴스에 대한 참조입니다.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

