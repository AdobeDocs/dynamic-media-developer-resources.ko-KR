---
description: 널
seo-description: 널
seo-title: 핫스팟 지원
solution: Experience Manager
title: 핫스팟 지원
topic: Dynamic media
uuid: 62e0e55a-55a3-417d-ad51-ec77a7c16ac3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 핫스팟 지원{#hotspot-support}

뷰어는 기본 보기 위쪽에 있는 핫스팟 아이콘 렌더링을 지원합니다. 핫스팟 아이콘의 모양은 핫스팟 섹션에 설명된 대로 CSS를 통해 제어됩니다.

핫스팟을 [참조하십시오](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

핫스팟은 JavaScript 콜백을 트리거하여 호스팅 웹 페이지에서 빠른 보기 기능을 활성화하거나 사용자를 외부 웹 페이지로 리디렉션할 수 있습니다.

## 빠른 보기 핫스팟 {#section-cda48fc9730142d0bb3326bac7df3271}

이러한 유형의 핫스팟은 Dynamic Media, AEM Assets on Demand의 &quot;빠른 보기&quot; 작업 유형을 사용하여 제작해야 합니다. 사용자가 이러한 핫스팟을 활성화하면 뷰어는 JavaScript `quickViewActivate` 콜백을 실행하고 핫스팟 데이터를 전달합니다. 포함 웹 페이지가 이 콜백을 수신해야 합니다. 페이지를 트리거하면 자체 빠른 보기 구현이 열립니다.

## 외부 웹 페이지로 리디렉션 {#section-ef820c71251e4215800bb99c0c9ebe16}

AEM 자산의 다이내믹 미디어에서 작업 유형 &quot;빠른 보기&quot;에 대해 제작된 핫스팟은 사용자를 외부 URL로 리디렉션합니다. 작성 중에 설정된 설정에 따라 URL은 새 브라우저 탭, 같은 창 또는 명명된 브라우저 창에서 열립니다.
