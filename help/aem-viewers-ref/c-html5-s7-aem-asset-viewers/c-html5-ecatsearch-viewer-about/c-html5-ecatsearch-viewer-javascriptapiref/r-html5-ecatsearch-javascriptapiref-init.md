---
description: eCatalog Viewer에 대한 JavaScript API 참조.
solution: Experience Manager
title: init
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog 검색
role: Developer,User
exl-id: 4d71062c-fee7-4339-bd7f-1b7f778465c4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 2%

---

# init{#init}

eCatalog Viewer에 대한 JavaScript API 참조.

[!DNL `init()`]

eCatalog 뷰어의 초기화를 시작합니다. 이 시간까지 컨테이너 DOM 요소를 만들어야 뷰어 코드가 ID로 찾을 수 있습니다.

컨테이너 요소가 웹 페이지 레이아웃의 일부가 아닌 경우(예: 이 요소에 지정된 [!DNL `display:none`] 스타일을 사용하여 숨길 수 있음) 뷰어는 웹 페이지가 컨테이너 요소를 다시 레이아웃으로 가져오는 시점까지 초기화 프로세스를 일시 중지합니다. 이런 경우 뷰어 로드가 자동으로 다시 시작됩니다.

뷰어 수명 주기 동안 이 메서드를 한 번만 호출합니다. 후속 호출은 무시됩니다.

## 매개 변수 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

없음.

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

[!DNL `{Object}`] 뷰어 인스턴스에 대한 참조입니다.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
