---
description: eCatalog 검색 뷰어는 기본 보기 위의 이미지 맵 아이콘 렌더링을 지원합니다.
seo-description: eCatalog 검색 뷰어는 기본 보기 위의 이미지 맵 아이콘 렌더링을 지원합니다.
seo-title: 이미지 맵 지원
solution: Experience Manager
title: 이미지 맵 지원
topic: Dynamic media
uuid: 22ba8168-b384-4eda-a147-ce8172cfed11
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 0%

---


# 이미지 맵 지원{#image-map-support}

eCatalog 검색 뷰어는 기본 보기 위의 이미지 맵 아이콘 렌더링을 지원합니다.

맵 아이콘의 모양은 [이미지 맵 효과](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289)에 설명된 대로 CSS를 통해 제어됩니다.

이미지 맵은 다음 3가지 작업 중 하나를 수행합니다.외부 웹 페이지, 정보 패널 팝업 활성화 및 내부 하이퍼링크로 이동합니다.

## 외부 웹 페이지 {#section-32ebe3c3a7f74892a428c5d48801de4d}로 리디렉션

이미지 맵의 `href` 속성에는 명시적으로 지정하거나 지원되는 JavaScript 템플릿 함수 중 하나로 래핑된 외부 리소스에 대한 URL이 있습니다.`loadProduct()`, `loadProductCW()` 및 `loadProductPW()`.

다음은 간단한 URL 리디렉션의 예입니다.

`href=http://www.adobe.com`

이 예에서 동일한 URL은 `loadProduct()` 함수로 래핑됩니다.

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

이미지 맵의 `HREF` 속성에 JavaScript 코드를 추가하면 클라이언트 컴퓨터에서 코드가 실행됩니다. 따라서 JavaScript 코드가 안전한지 확인하십시오.

## 정보 패널 팝업 활성화 {#section-7aa036420af646d1ad8cdc388add0b57}

[정보] 패널로 작업하기 위해 이미지 맵에는 `ROLLOVER_KEY` 속성 집합이 있습니다. 또한 `href` 속성을 동시에 설정해야 합니다. 그렇지 않으면 외부 URL 처리가 [정보] 패널 팝업 활성화를 방해합니다.

마지막으로 뷰어 구성에 `InfoPanelPopup.template` 및 선택적으로 `InfoPanelPopup.infoServerUrl` 매개 변수에 적절한 값이 포함되어 있는지 확인합니다.

>[!NOTE]
>
>정보 패널 팝업을 구성할 때 정보 패널에 전달되는 HTML 코드 및 JavaScript 코드는 클라이언트의 컴퓨터에서 실행됩니다. 따라서 이러한 HTML 코드와 JavaScript 코드가 안전한지 확인하십시오.

## 내부 하이퍼링크 {#section-6afa4fb2fe564c429e0201f019a95849}

이미지 맵을 클릭하면 뷰어 내에서 내부 페이지 교체가 수행됩니다. 이 기능을 사용하려면 이미지 맵에 있는 `href` 속성의 형식은 다음과 같습니다.

` href=target: *`idx`*`

여기서 ` *`idx`*`은(는) 카탈로그 스프레드의 인덱스(0부터 시작)입니다.

다음은 eCatalog의 3D 스프레드를 가리키는 이미지 맵에 대한 `href` 속성의 예입니다.

`href=target:2`
