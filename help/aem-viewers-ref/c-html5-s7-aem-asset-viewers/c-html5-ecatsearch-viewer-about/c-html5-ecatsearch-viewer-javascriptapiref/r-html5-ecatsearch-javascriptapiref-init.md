---
title: init
description: eCatalog 뷰어에 대한 JavaScript API 참조입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 4d71062c-fee7-4339-bd7f-1b7f778465c4
TQID: 'https://experienceleague.adobe.com/Hb-C6aORHF8--oX3IqgRZIi1rfbLg39F0Ewzb4sg45U'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 2%

---

# init{#init}

eCatalog 뷰어에 대한 JavaScript API 참조입니다.

[!DNL `init()`]

eCatalog 뷰어의 초기화를 시작합니다. 이때까지 뷰어 코드가 해당 ID로 찾을 수 있도록 컨테이너 DOM 요소를 만들어야 합니다.

컨테이너 요소가 아직 웹 페이지 레이아웃의 일부가 아닌 경우(예: 할당된 [!DNL `display:none`] 스타일을 사용하여 숨길 수 있는 경우) 뷰어는 초기화 프로세스를 일시 중단합니다. 웹 페이지가 컨테이너 요소를 레이아웃으로 다시 가져오는 순간까지 그렇게 됩니다. 이 이벤트가 발생하면 뷰어 로드가 자동으로 다시 시작됩니다.

뷰어 라이프사이클 중에 이 메서드를 한 번만 호출하면 됩니다. 이후의 호출은 무시됩니다.

## 매개 변수 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

없음.

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

[!DNL `{Object}`] 뷰어 인스턴스에 대한 참조입니다.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
