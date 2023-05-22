---
title: 호환성 정보
description: 운영 체제, 브라우저 및 모바일 장치에 대한 호환성 정보입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 7ad499b1-7da6-483b-ab11-cff2eb9271da
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 0%

---

# 호환성 정보{#compatibility-notes}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

운영 체제, 브라우저 및 모바일 장치에 대한 호환성 정보입니다.

## 블랙베리® {#section-0c465ac3775d47fd838e2695a00abc45}

* 이전 응용 비디오 세트와 호환되지 않습니다. 재생을 허용하려면 적응형 비디오 세트를 재업로드하십시오.

## 일반 {#section-7b9a9fcba85148d1802b7b3016b48e02}

* 브라우저 쪽 크기 조절로 인해 사용자가 페이지를 확대하면 UI 및 이미지가 흐릿해집니다. 사용자 인터페이스 서식은 확대/축소에 따라 잘못 표시되며 전체 화면으로 이동합니다.
* 모바일 장치의 크기 제한으로 인해 혼합 미디어 뷰어는 슬라이드 제스처를 사용하여 포함된 견본 구성 요소를 탭하는 대신 포함된 이미지 세트의 프레임을 전환합니다. 구성 요소가 시각적 표시기로 표시됩니다.
* Internet Explorer 브라우저 및 일부 터치 장치에서 전체 화면 모드는 전체 장치 화면을 차지하지 않습니다. 대신 브라우저 창의 크기로 응용 프로그램의 크기를 조정합니다.
* 닫기 버튼은 iOS 8.0 및 iOS 8.1에서는 작동하지 않지만 iOS 8.2에서는 작동합니다.

## 갤럭시 {#section-dfd5f46f39834223b544b1e2f7a770c1}

* 확대/축소 및 eCatalog 뷰어에 메모리 누수가 표시되었습니다. 프레임을 반복해서 탐색하면 브라우저가 충돌합니다.
* 뷰어를 두 번 탭하면 브라우저측 확장이 활성화된 뷰어가 아닌 전체 페이지가 확대/축소됩니다.

## 갤럭시 {#section-7effabfea75b488399e0f71cab4ce76b}

* 브라우저 설정에서 전체 화면 을 선택한 상태로 장치가 세로 모드에서 태블릿으로 감지되었습니다.

## 갤럭시 넥서스 {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* 뷰어를 두 번 탭하면 브라우저측 확장이 활성화된 상태에서 뷰어만 아닌 전체 페이지가 확대/축소됩니다.

## Galaxy Nexus 10 및 갤럭시 태블릿 {#section-ef52bd1249fe4f358c11838f7a557a00}

* 전자 카탈로그에 세로 및 가로 방향의 잘못된 페이지 스프레드가 표시됩니다.

## HTC 모바일 장치 {#section-dc42c80414c842e488738fc157c55b01}

* 기본 핀치 확대/축소를 비활성화하지 못하는 것은 HTC UI 래퍼(HTC 센스)의 &quot;기능&quot;입니다. 이 기능은 뷰어에서 &quot;핀치 투 줌&quot; 제스처를 사용할 때 전체 페이지가 확대/축소되도록 할 수 있습니다. 대신 두 번 누르기 제스처를 사용하십시오.
* 이미지 맵이 작고 서로 가까울 경우 이미지 맵 아이콘이 겹칩니다.

## HTML5 비디오 뷰어 {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` 수정자는 소프트웨어 HLS 및 Flash HDS 재생에서만 지원됩니다. 재생이 기본 플레이어를 사용하는 경우 작동하지 않습니다.
* OGG 및 WebM 점진적 재생은 지원되지 않습니다.
* 브라우저 크기 조정으로 인해 비디오 플레이어가 잘못된 크기로 표시됩니다(Windows® Campaign 컨트롤 패널 표시 설정 포함).
* Safari에서 HLS 스트리밍을 사용하는 비디오 추적이 일관되지 않습니다.

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* Quirks 모드는 지원되지 않습니다.
* 호환 모드는 지원되지 않습니다.
* 모바일의 Internet Explorer는 지원되지 않습니다.

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* 대형 eCatalogs로 인해 브라우저가 iPad 2에서 충돌합니다.

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1 이상: 인터넷 플러그인 설정으로 인해 Flash 비디오가 재생되지 않습니다.
* Safari에서 HLS 스트리밍을 사용하는 비디오 추적이 일관되지 않습니다.
* HLS 스트리밍을 사용하여 Safari 6에서 비디오의 끝을 찾을 수 없습니다.
