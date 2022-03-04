---
description: 이미지 제공 서비스는 소스 데이터로 확장 가능한 벡터 그래픽(SVG) 파일을 지원합니다. SVG 1.1을 준수해야 합니다.
solution: Experience Manager
title: SVG 지원
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 60e40195-710f-4f03-b152-52eaa10c5b21
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 0%

---

# SVG 지원{#svg-support}

이미지 제공 서비스는 소스 데이터로 확장 가능한 벡터 그래픽(SVG) 파일을 지원합니다. SVG 1.1을 준수해야 합니다.

이미지 제공 기능은 정적 SVG 콘텐츠만 인식합니다. 애니메이션, 스크립팅 및 기타 대화형 컨텐츠는 지원되지 않습니다.

SVG은 이미지 파일이 허용되는 모든 위치(URL 경로, `src=`, 및 `mask=`). SVG 파일의 컨텐츠가 래스터화된 후에는 이미지와 같이 처리됩니다.

이미지와 유사하게 SVG 파일을 이미지 카탈로그 항목으로 지정하거나 상대 파일 경로로 지정할 수 있습니다.

## 대체 변수 {#section-83b149f13f244193901df39b204c975b}

` $ *[!DNL var]*$` 대체 변수는 값 문자열의 SVG 파일에 포함할 수 있습니다. `<text>` 요소 및 모든 요소 속성.

포함된 이미지 제공 요청의 쿼리 부분에 있는 중요 변수는 직접 대체되지 않습니다. 대신, 사용 가능한 모든 변수 정의가 요청에 추가되므로 요청을 구문 분석할 때 이미지 제공 기능이 변수를 대체할 수 있습니다.

자세한 내용은 [대체 변수](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a) 추가 정보.

## 이미지 참조 {#section-a7680f9e6aca4b1a83560637cc9fac66}

이미지는 `<image>` 요소를 생성하지 않습니다. 에서 참조하는 이미지 `xlink::href` 의 속성 `<image>` 요소는 올바른 이미지 제공 요청이어야 합니다. 외부 URL은 허용되지 않습니다.

다음으로 시작하는 전체 이미지 제공 요청을 지정합니다. `http://`, 또는 다음으로 시작하는 상대 url `/is/image`. 전체 HTTP 경로를 지정하면 경로에서 도메인 이름이 제거되어 상대 형식으로 변환됩니다. 타사 SVG 렌더러를 사용하여 파일을 미리 볼 수 있으므로 전체 HTTP 경로를 사용하는 것이 유용할 수 있습니다.

>[!NOTE]
>
>이 릴리스의 이미지 제공 서비스에서는 이미지 렌더링에 대한 지원이 제한됩니다. SVG 내에서 이미지를 참조하는 것은 기존의 이미지 제공 계층화 및 템플릿 메커니즘이 원하는 결과를 달성하는 데 부족한 경우에만 사용해야 합니다. 어떠한 경우에도 다중 이미지 복합체를 생성하는 데 SVG을 사용해야 합니다.

>[!NOTE]
>
>SVG에 포함된 이미지의 크기가 현재 자동으로 조정되지 않습니다. 모든 이미지 히트에 원하는 이미지 크기를 설정하는 데 필요한 이미지 제공 명령이 포함되어 있는지 확인합니다(예: `wid=`). 이미지 크기를 명시적으로 설정하지 않으면 `attribute::DefaultPix` 이 적용됩니다.

## 색상 관리 {#section-ea76e2bc4e1842638aa97a2d470c8a68}

대체 변수를 통해 SVG 파일에 포함되고 SVG 템플릿에 전달되는 모든 색상 값은 `sRgb` 색상 공간.

이미지를 SVG에 포함할 때에는 색상 변환이 수행되지 않습니다. 색상 정확성을 보장하려면 `icc=sRgb` 모든 포함된 이미지 요청에 대해 해당됩니다.

래스터화 후 SVG 이미지는 다른 이미지와 마찬가지로 색상 관리에 참여합니다.

## 예 {#section-036cdd45abd449849ee00a8f21788c28}

다음 SVG 템플릿은 이미지 참조 및 변수 사용을 보여줍니다.

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

이 SVG 템플릿은 다음과 같이 사용할 수 있습니다.

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## 제한 사항 {#section-daa5eccd07204aaf993be41e87822d54}

SVG 파일은 독립형 파일이어야 하며, 이미지 제공 또는 이미지 렌더링 요청에서 참조되는 외부 이미지를 제외하고 보조 파일 또는 리소스를 참조해서는 안 됩니다(위 참조).

정적 콘텐츠만 렌더링됩니다. 애니메이션, 단추 등의 대화형 기능 존재할 수 있지만 예상대로 렌더링되지 않을 수 있습니다.

현재 ICC 프로필 기반 색상 사양은 지원되지 않습니다.

`<script>` 요소가 있을 수 있지만 항상 무시됩니다.

## 참조 {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [마스크=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [SVG 1.1 사양](https://www.w3.org/TR/SVG11/)
