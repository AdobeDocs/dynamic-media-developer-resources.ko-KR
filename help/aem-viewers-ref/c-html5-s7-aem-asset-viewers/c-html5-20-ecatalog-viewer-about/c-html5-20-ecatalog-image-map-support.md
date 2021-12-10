---
title: 이미지 맵 지원
description: eCatalog 뷰어는 기본 보기 위에 있는 이미지 맵 아이콘 렌더링을 지원합니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 7a2a58f9-852e-4205-96bc-08332507b6cd
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 0%

---

# 이미지 맵 지원{#image-map-support}

eCatalog 뷰어는 기본 보기 위에 있는 이미지 맵 아이콘 렌더링을 지원합니다.

맵 아이콘의 모양은 다음에 설명된 대로 CSS를 통해 제어됩니다. [이미지 맵 효과](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289).

이미지 맵은 다음 세 가지 작업 중 하나를 수행합니다. 외부 웹 페이지, 정보 패널 팝업 활성화 및 내부 하이퍼링크로 리디렉션합니다.

## 외부 웹 페이지로 리디렉션 {#section-32ebe3c3a7f74892a428c5d48801de4d}

다음 `href` 이미지 맵의 속성에는 명시적으로 지정하거나 지원되는 JavaScript 템플릿 함수 중 하나에 래핑된 외부 리소스에 대한 URL이 있습니다. `loadProduct()`, `loadProductCW()`, 및 `loadProductPW()`.

다음은 단순 URL 리디렉션의 예입니다.

`href=http://www.adobe.com`

이 예에서 동일한 URL은 `loadProduct()` 함수:

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

JavaScript 코드를 `HREF` 이미지 맵의 속성, 코드는 클라이언트의 컴퓨터에서 실행됩니다. 따라서 JavaScript 코드가 안전한지 확인하십시오.

## 정보 패널 팝업 활성화 {#section-7aa036420af646d1ad8cdc388add0b57}

정보 패널을 사용하여 작업하려면 이미지 맵에 `ROLLOVER_KEY` 속성 집합입니다. 또한, `href` 속성을 동시에 사용하여 외부 URL 처리가 [정보] 패널 팝업 활성화를 방해합니다.

마지막으로, 뷰어 구성에 `InfoPanelPopup.template` 그리고 선택적으로 `InfoPanelPopup.infoServerUrl` 매개 변수.

>[!NOTE]
>
>정보 패널 팝업을 구성하면 정보 패널에 전달된 HTML 코드 및 JavaScript 코드가 클라이언트의 컴퓨터에서 실행됩니다. 따라서 이러한 HTML 코드와 JavaScript 코드가 안전한지 확인하십시오.

## 내부 하이퍼링크 {#section-6afa4fb2fe564c429e0201f019a95849}

이미지 맵을 선택하면 뷰어 내에서 내부 페이지 교환이 수행됩니다. 이 기능을 사용하려면 `href` 이미지 맵의 속성에는 다음과 같은 특수 형식이 있습니다.

` href=target: *`idx`*`

위치 `*`idx`*` 카탈로그 확산의 0기반 색인입니다.

다음은 의 예입니다 `href` eCatalog의 3D 스프레드를 가리키는 이미지 맵에 대한 속성입니다.

`href=target:2`
