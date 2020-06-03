---
description: 운영 체제, 브라우저 및 모바일 디바이스에 대한 호환성 정보
seo-description: 운영 체제, 브라우저 및 모바일 디바이스에 대한 호환성 정보
seo-title: 호환성 정보
solution: Experience Manager
title: 호환성 정보
topic: Dynamic media
uuid: cf732a03-bfaa-4838-862f-73343cefbd67
translation-type: tm+mt
source-git-commit: a0983053795cc119eb57386c005e1f8a7c2fa3e4
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 1%

---


# 호환성 정보{#compatibility-notes}

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

운영 체제, 브라우저 및 모바일 디바이스에 대한 호환성 정보

## Blackberry {#section-0c465ac3775d47fd838e2695a00abc45}

* 이전 응용 비디오 세트와 호환되지 않습니다. 재생을 허용하려면 응용 비디오 세트를 다시 업로드해야 할 수 있습니다.

## 일반 {#section-7b9a9fcba85148d1802b7b3016b48e02}

* 사용자가 페이지를 확대/축소하면 브라우저 쪽 크기 조정으로 UI 및 이미지가 흐려질 수 있습니다. 확대/축소에 따라 UI 서식이 잘못 표시될 수도 있습니다. 전체 화면으로 넘어갑니다.
* 모바일 장치의 크기 제한으로 인해 혼합 미디어 뷰어는 포함된 견본 구성 요소를 탭하는 대신 슬라이드 제스처를 사용하여 포함된 이미지 세트의 프레임을 바꿉니다. 구성 요소는 시각적 표시기로 있습니다.
* Internet Explorer 브라우저와 일부 터치 장치에서는 전체 화면 모드가 장치 화면을 차지하지 않습니다. 대신 응용 프로그램의 크기를 브라우저 창 크기로 조정합니다.
* iOS 8.0 및 iOS 8.1에서는 닫기 단추가 작동하지 않지만 iOS 8.2에서는 작동합니다.

## Galaxy SIII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* 확대/축소 및 eCatalog 뷰어에서 메모리 누수가 발견되었습니다. 프레임을 탐색하는 경우 브라우저가 충돌할 수 있습니다.
* 뷰어를 두 번 누르면 브라우저 쪽 크기 조절이 활성화된 뷰어가 아니라 전체 페이지가 확대/축소할 수 있습니다.

## Galaxy S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* 브라우저 설정에서 전체 화면이 선택된 상태로 장치가 세로 모드에서 태블릿으로 검색되었습니다.

## 갤럭시 넥서스 {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* 뷰어를 두 번 누르면 브라우저 측 크기 조정 기능이 활성화된 상태에서 뷰어만 확대되는 대신 전체 페이지가 확대/축소될 수 있습니다.

## 갤럭시 넥서스 10 및 갤럭시 태블릿 {#section-ef52bd1249fe4f358c11838f7a557a00}

* 전자 카탈로그는 세로 및 가로 방향의 잘못된 페이지 스프레드를 표시합니다.

## HTC 모바일 장치 {#section-dc42c80414c842e488738fc157c55b01}

* 기본 손가락을 모으고 펴서 확대/축소를 비활성화하지 못하는 것은 HTC UI 래퍼(HTC Sense)의 &quot;기능&quot;입니다. 이 기능을 사용하면 뷰어에서 &quot;확대/축소&quot; 제스처를 사용할 때 전체 페이지를 확대/축소할 수 있습니다. 대신 두 번 누르기 제스처를 사용하십시오.
* 이미지 맵이 작고 함께 닫히면 이미지 맵 아이콘이 겹칠 수 있습니다.

## HTML5 Video Viewer {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` modifier는 소프트웨어 HLS 및 flash HDS 재생에서만 지원됩니다. 재생이 기본 플레이어를 사용하는 경우에는 작동하지 않습니다.
* OGG 및 WebM 점진적 재생은 지원되지 않습니다.
* 브라우저 크기 조정으로 인해 비디오 플레이어가 잘못된 크기로 표시될 수 있습니다(Windows OS 제어판 표시 설정 포함).
* Safari에서 HLS 스트리밍을 사용하는 비디오 검색이 일관되지 않을 수 있습니다.

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* Quirks 모드는 지원되지 않습니다.
* 호환성 모드는 지원되지 않습니다.
* 모바일의 Internet Explorer는 지원되지 않습니다.

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* 큰 eCatalogs로 인해 iPad 2에서 브라우저가 충돌할 수 있습니다.

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1 이상: 인터넷 플러그인 설정으로 인해 Flash 비디오가 재생되지 않을 수 있습니다.
* Safari에서 HLS 스트리밍을 사용하는 비디오 검색이 일관되지 않을 수 있습니다.
* HLS 스트리밍을 사용하여 Safari 6에서 비디오를 종료할 수 없습니다.

