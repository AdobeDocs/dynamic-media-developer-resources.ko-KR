---
title: 핫스팟 및 이미지 맵 지원
description: 핫스팟 및 이미지 맵 지원
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: b441e241-809e-47cf-a309-57283bd0532b
TQID: 'https://experienceleague.adobe.com/lXiW-xoAeHFZic9fH-AN491yZfrPE1R0S53FBS1oMig'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 212
ht-degree: 0%

---

# 핫스팟 및 이미지 맵 지원{#hotspot-and-image-maps-support}

뷰어는 기본 보기의 맨 위에 핫스팟 아이콘 및 이미지 맵 영역의 렌더링을 지원합니다. 핫스팟 아이콘 및 영역의 모양은 핫스팟 및 이미지 맵 사용자 지정 섹션에 설명된 대로 CSS를 통해 제어됩니다.

[핫스팟 및 이미지 맵](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74)을 참조하십시오.

핫스팟 및 영역은 JavaScript 콜백을 트리거하여 호스팅 웹 페이지에서 빠른 보기 기능을 활성화하거나 사용자를 외부 웹 페이지로 리디렉션할 수 있습니다.

## 핫스팟 빠른 보기 {#section-cda48fc9730142d0bb3326bac7df3271}

이러한 유형의 핫스팟 또는 이미지 맵은 Adobe Experience Manager의 Dynamic Media에 있는 &quot;빠른 보기&quot; 작업 유형을 사용하여 작성해야 합니다. 사용자가 이러한 핫스팟 또는 이미지 맵을 활성화하면 뷰어가 `quickViewActivate` JavaScript 콜백을 실행하고 핫스팟 또는 이미지 맵 데이터를 전달합니다. 포함 웹 페이지는 이 콜백을 수신해야 합니다. 페이지가 트리거되면 고유한 빠른 보기 구현이 열립니다.

## 외부 웹 페이지로 리디렉션 {#section-ef820c71251e4215800bb99c0c9ebe16}

Experience Manager의 Dynamic Media에서 작업 유형 &quot;빠른 보기&quot;로 작성된 핫스팟 또는 이미지 맵은 사용자를 외부 URL로 리디렉션합니다. 작성 중에 설정된 설정에 따라 URL이 새 브라우저 탭, 동일한 창 또는 명명된 브라우저 창에서 열립니다.
