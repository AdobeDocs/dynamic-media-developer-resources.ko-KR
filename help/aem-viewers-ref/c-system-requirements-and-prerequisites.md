---
title: Dynamic Media HTML5 뷰어에 대한 시스템 요구 사항
description: Dynamic Media HTML5 뷰어에 대한 시스템 요구 사항입니다.
solution: Experience Manager
contentOwner: Rick Brough
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: e4543358-92a6-4acc-a8a2-227e1daea722
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 2%

---

# Dynamic Media HTML5 뷰어 시스템 요구 사항{#system-requirements}

Dynamic Media HTML5 뷰어에 대한 시스템 요구 사항입니다.

<!-- Updated March 03, 2022 Contact is now Deepa Gupta -->

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## 서버 하드웨어 및 소프트웨어 {#section-05099146f1f0418988c196635110bee6}

<!-- Updated March 03, 2022 Contact is now Deepa Gupta -->

* Adobe Dynamic Media 이미지 제공 6.7.1 이상
* HTML5 뷰어에는 SDK JavaScript 서버측 라이브러리 3.11.5 이상이 필요합니다.
* *친구에게 이메일 보내기* 소셜 기능에는 s7ondemand 5.0.9 이상이 필요합니다.
* eCatalog 뷰어 - [정보 패널 팝업](/help/aem-viewers-ref/c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-infopanelpopup.md) 지원을 사용하려면 정보 서버 2.1.8 이상이 필요합니다.
* 검색 기능 구성 요소에는 s7search 2.3.0 이상이 필요합니다.

## 뷰어 시스템 요구 사항 {#section-cc72b1e209524d038b4d5b92b35e998e}

**구성 요소 뷰어에 대한 클라이언트 브라우저 최소 요구 사항:**

* 다음 운영 체제 버전 이상에서 지원됩니다.
   * Microsoft® Windows® 7
   * macOS x 10.12
* 다음 브라우저/플랫폼 버전 이상에서 지원됩니다.
   * Android™ OS 4.x
   * BlackBerry® 10(기본 브라우저) 비디오 재생만 지원됩니다.
   * Chrome
   * Edge
   * 파이어폭스
   * Internet Explorer 11
   * iOS
   * iPad 2(Safari 및 Chrome 브라우저만 해당)
   * iPhone
   * Safari 11
* 모바일 장치의 Internet Explorer는 지원되지 않습니다.
* *PanoramicViewer*&#x200B;는 다음 브라우저/플랫폼 버전 이상에서 지원됩니다.
   * Android™ 4.4(전화 장치만 해당)
   * Chrome
   * Edge
   * 파이어폭스
   * Internet Explorer 11
   * iOS 10
   * Safari 11
* *Video360Viewer* 및 *DimensionalViewer*&#x200B;은(는) 다음 브라우저/플랫폼 버전 이상에서 지원됩니다.
   * Android™ 5(전화 장치만 해당)
   * Chrome
   * Edge
   * 파이어폭스
   * iOS 12
   * Safari 12
* *ZoomVerticalViewer*&#x200B;는 다음 브라우저/플랫폼 버전 이상에서 지원됩니다.
   * Android™ 4.x
   * Chrome
   * Edge
   * 파이어폭스
   * Internet Explorer 11
   * iOS 10
   * Safari 11

## TLS 1.0 및 1.1 지원 종료 {#tls}

<!-- CQDOC-19433 -->

2022년 9월 30일부터 Adobe Dynamic Media 뷰어에 대한 지원이 종료되었습니다.

* TLS(전송 계층 보안) 1.0 및 1.1
* TLS 1.2의 약한 암호는 다음과 같습니다.
   * TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384
   * TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA
   * TLS_RSA_WITH_AES_256_GCM_SHA384
   * TLS_RSA_WITH_AES_256_CBC_SHA256
   * TLS_RSA_WITH_AES_256_CBC_SHA
   * TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256
   * TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA
   * TLS_RSA_WITH_AES_128_GCM_SHA256
   * TLS_RSA_WITH_AES_128_CBC_SHA256
   * TLS_RSA_WITH_AES_128_CBC_SHA
   * TLS_RSA_WITH_CAMELIA_256_CBC_SHA
   * TLS_RSA_WITH_CAMELIA_128_CBC_SHA
   * TLS_ECDHE_RSA_WITH_3DES_EDE_CBC_SHA
   * TLS_RSA_WITH_SDES_EDE_CBC_SHA

## Dynamic Media 뷰어에 지원되지 않는 웹 브라우저 및 운영 체제 조합 {#browser-os-support}

<!-- CQDOC-19433 -->

Adobe Dynamic Media 뷰어는 다음 웹 브라우저 및 운영 체제 조합을 지원하지 않습니다.

* Internet Explorer 11 + Windows 7
* Internet Explorer 11 + Windows 8.1
* Internet Explorer 11 + Windows Phone 8.1
* Internet Explorer 11 + Windows Phone 8.1 업데이트
* Safari 6 + iOS 6.0.1
* Safari 7 + iOS 7.1
* Safari 7 + OS X 10.9 Mavericks
* Safari 8 + iOS 8.4
* Safari 8 + OS X 10.10 Yosemite

<!-- CQDOC-19433 -->

<!-- 
NOTE
Effective September 30, 2018, Adobe Dynamic Media Classic Viewers ended support of Transport Layer Security 1.0 (TLS 1.0). As such, Dynamic Media Classic no longer supports viewers on the following browsers/platforms that support TLS 1.0 (Adobe recommends using TLS 1.2 or later):

* Android&trade; 2.3.7
* Android&trade; 4.0.4
* Android&trade; 4.1.1
* Android&trade; 4.2.2
* Android&trade; 4.3
* Internet Explorer 7 on Window Vista&reg;
* Internet Explorer 8 on Windows&reg; XP
* Internet Explorer 8-10 on Windows&reg; 7
* Internet Explorer 10 on Windows&reg; Phone 8.0
* Safari 5.1.9 on Apple OS X 10.6.8
* Safari 6.0.4 on Apple OS X 10.8.4
* Java&trade; 6u45
* Java&trade; 7u25
* OpenSSL 0.9.8y
* Baidu January 2015

NOTE
FLASH VIEWERS END-OF-LIFE — Effective January 31, 2017, Adobe Dynamic Media Classic officially ended support for the Flash viewer platform. -->

