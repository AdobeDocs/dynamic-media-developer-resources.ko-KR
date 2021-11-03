---
description: 스마트 자르기 비디오 뷰어에 대한 JavaScript API 참조.
solution: Experience Manager
title: dispose
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: c4bcccdc-6f23-4213-a1d1-03c5c62ba484
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---

# dispose{#dispose}

스마트 자르기 비디오 뷰어에 대한 JavaScript API 참조.

`dispose()`

뷰어 논리에서 사용되는 모든 리소스를 해제하고 런타임에 뷰어가 만든 모든 내부 개체 및 구성 요소를 삭제하여 이 뷰어 인스턴스를 삭제합니다.

웹 페이지 코드도 뷰어 인스턴스 변수를 삭제하고 웹 브라우저 메모리에서 뷰어를 완전히 제거해야 합니다.

웹 페이지 코드가 뷰어 SDK 구성 요소에서 직접 또는 이러한 구성 요소에 저장된 외부 참조를 사용하여 이벤트 리스너를 등록한 경우, 이러한 리스너는 웹 페이지 코드에 의해 명시적으로 등록되지 않은 상태여야 하며, 이러한 외부 구성 요소 참조는 호출 전에 삭제해야 합니다 `dispose()`.

이후에 더 이상 뷰어 API에 액세스하지 마십시오 `dispose()` 가 호출됩니다.

## 매개 변수 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

없음.

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
