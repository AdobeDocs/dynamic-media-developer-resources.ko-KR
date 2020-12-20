---
description: 이 섹션의 설정은 SVG 렌더링이 필요한 경우에만 고려해야 합니다.
seo-description: 이 섹션의 설정은 SVG 렌더링이 필요한 경우에만 고려해야 합니다.
seo-title: SVG
solution: Experience Manager
title: SVG
topic: Scene7 Image Serving - Image Rendering API
uuid: 9e69b150-46ac-480f-96db-afadccc40fe4
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 1%

---


# SVG{#svg}

이 섹션의 설정은 SVG 렌더링이 필요한 경우에만 고려해야 합니다.

## SV::SvgHeapSize - SVG 더미 크기 {#section-59ab17681daa4be8b5d794713e1a504e}

SVG 렌더러의 Java 더미 크기입니다. 기본값은 &quot;200m&quot;(200MB)입니다.

## PS::svgProvider.rootPaths - SVG 데이터 루트 폴더 {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

SVG 소스 데이터 파일의 위치입니다. *[!DNL install_folder]*&#x200B;에 상대적인 하나 이상의 절대 파일 경로 또는 경로가 세미콜론으로 구분될 수 있습니다. 일반적으로 `IS::RootPath`과 동일한 값으로 설정됩니다.

## PS::svgProvider.SVGFileSizeLimit - 최대 SVG 파일 크기 {#section-b9c81e3e104642ebbdd9f000843d3256}

최대 SVG 소스 파일 크기(kBytes)입니다. 이 제한보다 큰 SVG 파일을 렌더링하려고 하면 서버에서 오류를 반환합니다. 기본값은 1024KB입니다.

## IS::SvgMAxRenderRgnPixels - SVG 출력 이미지 크기 제한 {#section-5be1fd9639424d878a5ffd11736d3920}

SVGRender가 생성할 수 있는 이미지 크기를 제한합니다. 수백만 픽셀의 정수 값이 0보다 큽니다. 렌더링 작업이 크기 제한을 초과할 경우 오류가 반환됩니다. 기본값은 4입니다.

## PS::svgProvider.port - 플랫폼 서버 수신 대기 포트 {#section-f7e42a96c2dd4523b46f0557c239e659}

SVG 렌더링에 포함할 플랫폼 서버에서 이미지를 가져오는 데 SvgRender에 사용되는 포트입니다.

중요 SVGRender 구성 요소의 올바른 기능을 수행하려면 이 구성 옵션을 `TC::PsPort`과(와) 동일한 값으로 설정해야 합니다.

## PS::svgProvider.fontRoot - SVG 글꼴 파일 폴더 {#section-a8d45b0d68504945b8780f5eac351b0d}

SVG 텍스트를 렌더링하는 데 필요한 글꼴 파일을 찾을 위치를 지정합니다.일반적으로 `IS::RootPaths`에 지정된 경로 중 하나입니다. 기본값은 [!DNL *[!DNL install_folder]*/images]입니다.

## SVG::SVGRender.port, IS::SVGTcpPort - SVG 통신 포트 {#section-608687123aa644b7b58fe42385d71b79}

이미지 서버와 SVGRender 구성 요소가 통신하는 포트를 구성합니다.

>[!NOTE]
>
>SVGRender 구성 요소의 올바른 기능을 위해서는 `SVG::SVGRender.port` 및 `IS::SVGTcpPort`에 대해 동일한 포트 번호를 지정해야 합니다.

