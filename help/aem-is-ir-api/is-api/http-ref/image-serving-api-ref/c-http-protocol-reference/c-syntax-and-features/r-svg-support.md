---
description: 이미지 제공은 SVG(Scalable Vector Graphics) 파일을 소스 데이터로 지원합니다. SVG 1.1을 준수해야 합니다.
seo-description: 이미지 제공은 SVG(Scalable Vector Graphics) 파일을 소스 데이터로 지원합니다. SVG 1.1을 준수해야 합니다.
seo-title: SVG 지원
solution: Experience Manager
title: SVG 지원
topic: Scene7 Image Serving - Image Rendering API
uuid: 30d7b37d-fdef-4518-a4b3-4baee56fa634
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SVG 지원{#svg-support}

이미지 제공은 SVG(Scalable Vector Graphics) 파일을 소스 데이터로 지원합니다. SVG 1.1을 준수해야 합니다.

이미지 제공은 정적 SVG 내용만 인식합니다.애니메이션, 스크립팅 및 기타 대화형 콘텐츠는 지원되지 않습니다.

SVG는 이미지 파일이 허용되는 모든 위치(URL 경로 `src=`및 `mask=`)에 지정할 수 있습니다. SVG 파일의 내용이 래스터화된 후 이미지와 같이 처리됩니다.

이미지와 유사하게 SVG 파일을 이미지 카탈로그 항목 또는 상대 파일 경로로 지정할 수 있습니다.

## 대체 변수 {#section-83b149f13f244193901df39b204c975b}

` $ *[!DNL var]*$` 대체 변수는 값 문자열 `<text>` 요소 및 모든 요소 속성의 SVG 파일에 포함될 수 있습니다.

포함된 이미지 제공 요청의 쿼리 부분에 있는 중요 변수는 직접 대체되지 않습니다. 대신, 사용 가능한 모든 변수 정의가 요청에 추가되어 요청을 구문 분석할 때 이미지 제공에서 변수를 대체할 수 있습니다.

자세한 [내용은 대체](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a) 변수를 참조하십시오.

## 이미지 참조 {#section-a7680f9e6aca4b1a83560637cc9fac66}

이미지를 `<image>` 요소를 사용하여 SVG에 삽입할 수 있습니다. 요소의 `xlink::href` 속성으로 참조되는 `<image>` 이미지는 올바른 이미지 제공 요청이어야 합니다. 외래 URL은 허용되지 않습니다.

다음으로 시작, 전체 이미지 제공 요청 `http://`또는 다음으로 시작하는 상대 URL을 지정합니다 `/is/image`. 전체 HTTP 경로를 지정하면 경로에서 도메인 이름이 제거되어 상대 형식으로 변환됩니다. 타사 SVG 렌더러를 사용하여 파일을 미리 볼 수 있으므로 전체 HTTP 경로를 사용하는 것이 유리할 수 있습니다.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>이 이미지 제공 릴리스의 이미지 렌더링에 대한 지원은 제한되어 있습니다. SVG 내에서 이미지를 참조하려면 기존 이미지 제공 레이어와 템플릿 메커니즘이 원하는 결과를 얻기에 부족한 경우에만 사용해야 합니다. 어떠한 경우에도 SVG를 사용하여 다중 이미지 합성을 생성할 수 없습니다.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>SVG에 포함된 이미지는 현재 자동으로 크기가 조정되지 않습니다. 모든 이미지 헤더에 원하는 이미지 크기(예: `wid=`). 이미지 크기가 명시적으로 설정되지 않으면 `attribute::DefaultPix` 적용됩니다.

## Color management {#section-ea76e2bc4e1842638aa97a2d470c8a68}

SVG 파일에 임베드되어 대체 변수를 통해 SVG 템플릿에 전달된 모든 색상 값이 `sRgb` 색상 공간에 존재하는 것으로 가정합니다.

이미지를 SVG에 포함할 때 색상 변환이 수행되지 않습니다. 색상을 그대로 유지하려면 포함된 모든 이미지 요청에 `icc=sRgb` 대해 지정해야 합니다.

래스터화 후 SVG 이미지는 다른 이미지와 마찬가지로 색상 관리에 참여합니다.

## 예 {#section-036cdd45abd449849ee00a8f21788c28}

다음 SVG 템플릿은 이미지 참조 및 변수 사용을 보여 줍니다.

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

이 SVG 템플릿은 다음과 같이 사용될 수 있습니다.

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## Restrictions {#section-daa5eccd07204aaf993be41e87822d54}

SVG 파일은 독립 실행형 파일이어야 하며, 이미지 제공 또는 이미지 렌더링 요청으로 참조되는 외부 이미지를 제외하고 보조 파일 또는 리소스를 참조해서는 안됩니다(위 참조).

정적 컨텐츠만 렌더링됩니다. 애니메이션, 버튼 등의 인터랙티브한 기능 있을 수 있지만 예상대로 제공할 수 없습니다.

현재 ICC 프로필 기반 색상 사양은 지원되지 않습니다.

`<script>` 요소는 존재하지만 항상 무시됩니다.

## 참조 {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [SVG 1.1 사양](http://www.w3.org/TR/SVG11/)
