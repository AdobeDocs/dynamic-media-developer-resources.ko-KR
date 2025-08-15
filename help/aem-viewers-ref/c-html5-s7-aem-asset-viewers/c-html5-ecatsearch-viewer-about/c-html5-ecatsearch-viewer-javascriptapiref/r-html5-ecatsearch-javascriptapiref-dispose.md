---
title: dispose
description: eCatalog 뷰어에 대한 JavaScript API 참조입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: fda6d50f-0e1b-436c-af2e-1ccc9cd51c39
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 3%

---

# dispose{#dispose}

eCatalog 뷰어에 대한 JavaScript API 참조입니다.

[!DNL `dispose()`]

뷰어 논리에서 사용하는 모든 리소스를 해제하고 런타임에 뷰어에서 만든 모든 내부 개체와 구성 요소를 삭제하여 이 뷰어 인스턴스를 삭제합니다.

웹 페이지 코드는 웹 브라우저 메모리에서 뷰어를 완전히 제거하려면 뷰어 인스턴스 변수도 삭제해야 합니다.

웹 페이지 코드가 뷰어에서 사용하는 Viewer SDK 구성 요소에 직접 이벤트 리스너를 등록했거나 이러한 구성 요소에 대한 외부 참조를 저장한 경우 이러한 리스너는 웹 페이지 코드에서 명시적으로 등록 취소해야 합니다. [!DNL `dispose()`]을(를) 호출하기 전에 이러한 외부 구성 요소 참조를 삭제해야 합니다.

[!DNL `dispose()`]이(가) 호출된 후에는 더 이상 뷰어 API에 액세스하지 마십시오.

## 매개 변수 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

없음.

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
