---
title: init
description: 대화형 비디오 뷰어에 대한 JavaScript API 참조입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 5fcc7dcd-a9a8-4a87-9c8d-42717ced8ae9
TQID: 'https://experienceleague.adobe.com/Wl6sRHW7Pv-MZxscPeDcxaAKzP1CqAT4RuWeS2-PCVk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 126
ht-degree: 2%

---

# init{#init}

대화형 비디오 뷰어에 대한 JavaScript API 참조입니다.

`init()`

대화형 비디오 뷰어의 초기화를 시작합니다. 이 시점까지 뷰어 코드가 해당 ID로 찾을 수 있도록 컨테이너 DOM 요소를 만들어야 합니다.

컨테이너 요소가 아직 웹 페이지 레이아웃의 일부가 아닌 경우(예: 할당된 `display:none` 스타일을 사용하여 숨길 수 있음) 뷰어가 초기화 프로세스를 일시 중단합니다. 웹 페이지가 컨테이너 요소를 레이아웃으로 다시 가져오는 순간까지 그렇게 됩니다. 이 이벤트가 발생하면 뷰어 로드가 자동으로 다시 시작됩니다.

이 메서드는 뷰어 수명 주기 동안 한 번만 호출합니다. 이후의 호출은 무시됩니다.

## 매개 변수 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

없음.

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 뷰어 인스턴스에 대한 참조입니다.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
