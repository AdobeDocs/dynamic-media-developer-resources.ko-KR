---
description: 핫스팟 및 이미지 맵 지원
solution: Experience Manager
title: 핫스팟 및 이미지 맵 지원
feature: Dynamic Media Classic,Viewers,SDK/API,회전 배너
role: Developer,User
exl-id: b441e241-809e-47cf-a309-57283bd0532b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# 핫스팟 및 이미지 맵 지원{#hotspot-and-image-maps-support}

뷰어는 기본 보기 상단에 핫스팟 아이콘 및 이미지 맵 영역의 렌더링을 지원합니다. 핫스팟 아이콘 및 영역의 모양은 핫스팟 및 이미지 맵 사용자 지정 섹션에 설명된 대로 CSS를 통해 제어됩니다.

[핫스팟 및 이미지 맵](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74)을 참조하십시오.

핫스팟과 영역은 JavaScript 콜백을 트리거하여 호스팅 웹 페이지에서 빠른 보기 기능을 활성화하거나 사용자를 외부 웹 페이지로 리디렉션할 수 있습니다.

## 빠른 보기 핫스팟 {#section-cda48fc9730142d0bb3326bac7df3271}

이러한 유형의 핫스팟이나 이미지 맵은 AEM의 Dynamic Media에 있는 &quot;빠른 보기&quot; 작업 유형을 사용하여 작성해야 합니다. 사용자가 이러한 핫스팟이나 이미지 맵을 활성화하면 뷰어가 `quickViewActivate` JavaScript 콜백을 실행하고 핫스팟 또는 이미지 맵 데이터를 이 맵에 전달합니다. 포함 웹 페이지가 이 콜백을 수신해야 합니다. 페이지를 트리거하면 자체 빠른 보기 구현이 열립니다.

## 외부 웹 페이지로 리디렉션 {#section-ef820c71251e4215800bb99c0c9ebe16}

AEM의 Dynamic Media에서 작업 유형 &quot;빠른 보기&quot;에 대해 작성된 핫스팟 또는 이미지 맵은 사용자를 외부 URL로 리디렉션합니다. 작성 중에 수행한 설정에 따라 URL이 새 브라우저 탭, 동일한 창 또는 명명된 브라우저 창에서 열립니다.
