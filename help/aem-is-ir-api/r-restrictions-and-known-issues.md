---
description: Scene7 이미지 제공 사용 시 고려해야 하는 몇 가지 제한 사항과 알려진 문제가 있습니다.
seo-description: Scene7 이미지 제공 사용 시 고려해야 하는 몇 가지 제한 사항과 알려진 문제가 있습니다.
seo-title: 제한 및 알려진 문제
solution: Experience Manager
title: 제한 및 알려진 문제
topic: Scene7 Image Serving - Image Rendering API
uuid: 9f9fad41-4828-4fba-8f5f-2c33e7811c71
translation-type: tm+mt
source-git-commit: 0e9d6a0ccbb040b27cc89b933442d8530c60d5c8
workflow-type: tm+mt
source-wordcount: '1248'
ht-degree: 0%

---


# 제한 및 알려진 문제{#restrictions-and-known-issues}

Scene7 이미지 제공 사용 시 고려해야 하는 몇 가지 제한 사항과 알려진 문제가 있습니다.

## 설명서 오류 {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* 줄 수는 `\copyfitmaxlines` 설정의 최대값과 텍스트 입력의 명시적 줄 수를 초과할 수 없습니다.
* 이미지 세트에 중괄호와 괄호가 일치해야 합니다. 중괄호와 괄호가 일치하지 않으면 URL로 인코딩되어야 합니다.
* 서버측 글로벌 응답 시간 경고에는 오류 응답이 포함됩니다.
* 이미지 또는 마스크 요청과 함께 `rect=` 명령을 사용할 때는 현재 `id=` 명령이 필요합니다.

## textPs= vs text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* 합성 이탤릭체는 `text=`을(를) 사용할 때보다 기울어진 상태로 렌더링됩니다.
* 밑줄이 `text=`을(를) 사용할 때보다 약간 작고 얇습니다.
* `\expnd` 그리고  `\expndtw` 음수 값이 높으면 사용할 때 문자가 서로 앞에 배치됩니다 `text=`.

* `\charscaley` 사용할 때와 다르게 크기 `text=` 를 조절하지만 선 높이에 영향을 주지 않습니다.

* 텍스트의 마지막 줄이 맞지 않으면 잘라내기로 표시되는 대신 전체 줄이 삭제됩니다.
* `\slmult` 그리고 MS Word 및  `\sl` 다른 방식으로  `text=`동작하면 현재 및 이후 단락에 적용됩니다.

* `\sb` 는 MS Word의 첫 번째 단락에 적용되며 Adobe InDesign과 Photoshop `text=`는 이 작업을 수행하지 않습니다.

* `\sa` 는 MS Word의 마지막 단락에 적용되며 Adobe InDesign과 Photoshop은  `text=`이를 수행하지 않습니다.

## 이전 버전과의 호환성 {#section-a76842f751944f4fb664af296d064122}

* RTF 문자열에서 밑줄 문자( `\_`)를 이스케이프 처리하는 것은 `textPs=`을 사용하여 모든 글꼴에서 작동하지 않습니다.

* 대/소문자를 구분하지 않는 매크로 처리를 지원합니다.
* 카탈로그 캐시가 60초에서 10초로 줄었습니다.
* 이제 오류 리디렉션 기능은 손상된 이미지, 글꼴, 색상 프로필 및 카탈로그에 게시되지만 디스크에 없는 이미지를 참조하는 요청만 리디렉션합니다.
* `posN=`,  `anchor=`,  `anchorN=`및  `origin=`  `originN=` 이제 수정자 값이 2147483648보다 큰 경우 구문 분석 오류를 반환합니다.

* 중첩 요청의 인코딩은 지원되지 않습니다. 새 동작으로 전환하고 사이트 및 회사 카탈로그의 URL 요청에 있는 중첩 요청 값을 인코딩하지 않습니다.
* 이제 `req=tmb`을(를) 사용할 때 DefaultImage가 축소판 속성을 적용합니다.
* `flip=`을(를) 사용하는 이전 버전에서는 기준점이 무엇이었는지에 관계없이 이미지가 다시 배치되지 않았습니다.

## 타사 라이브러리 {#section-79768b96bf634e44ab672c5b893f343d}에 적용되는 제한 사항

Digimarc 라이브러리는 Digimarc 워터마크가 이미 감지된 경우 이미지에 적용되지 않습니다. 기본 이미지에 충분한 편집 작업을 수행한 경우 Digimarc 라이브러리는 워터마크가 적용되었음을 인식할 수 있습니다. 그러나 해당 정보를 읽을 수 없을 수도 있습니다. 이렇게 하면 원래 이미지에 적용된 원본 Digimarc 정보를 가져올 수 없는 새 이미지가 만들어집니다. 이제 이미지 제공에서 회사 카탈로그에 정의된 Digimarc 워터마크를 적용할 수 있습니다.

## 이미지 제공 및 이미지 렌더링 모두에 적용 가능한 제한 사항 {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* 4개 이상의 CPU를 사용할 수 있는 경우 이미지 제공 및 이미지 렌더링은 모든 CPU의 이점을 충분히 활용하지 못할 수 있습니다. 이러한 시스템의 트래픽을 시뮬레이션하여 4개 이상의 CPU에서 트래픽이 얼마나 유용한지 확인할 수 있습니다.
* 리디렉션(HTTP 상태 301, 302 또는 303)을 반환하는 원격 URL은 거부됩니다.
* `errorRedirect.rootUrl`을 구성할 때 이 속성에 정의된 IP 주소는 해당 서버의 규칙 세트 `<addressfilter>` 태그 값에 포함되어야 합니다.

   *예*:

   서버 A가 `errorRedirect.rootUrl=10.10.10.10`을(를) 정의했습니다.

   IP 주소가 10.10.10.10인 서버 B는 규칙 세트 파일에 `<addressfilter>` 태그 값을 설정하여 해당 IP 주소(10.10.10.10)을 포함합니다.

* 위치가 지정된 점 텍스트 및 텍스트 패스는 클리핑을 나타낼 수 있습니다.
* `text=` 단락 `\sa` 이 아닌 전체 텍스트 블록 `\sb` 에 적용되는 경우에만 해당됩니다.

* URL에 정의된 회사와 `src=` 또는 `mask=` 수정자에 대해 정의된 다른 회사를 사용할 때는 이 작업 요청 양식을 위해 `src=` 또는 `mask=`에 대해 정의된 회사에 슬래시(/)를 접두사로 추가해야 합니다.

   *예*:

   `/is/image/MyCompany?src=/YourCompany/MyImage` .

   대신:`/is/image/MyCompany?src=YourCompany/MyImage` .

* 비피라미드형 Tiff 또는 비네팅 요청은

   *&quot;이미지 `C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt` 에 유효한 DSF가 없으며 2.25MPixel의 영역이 2MPixel의 최대값을 초과합니다&quot;* .

   피라미드 스티프와 비네팅을 사용하는 것이 가장 좋습니다. 비피라미드형 tiff 또는 비네팅을 사용해야 하는 경우에는 아래 지침에 따라 크기 제한을 늘리십시오.

   *작업 영역*:

   비네팅이 아닌 이미지 렌더링의 경우 [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml] 구성 파일의 IrMaxNonPyrVignetteSize 속성 값을 늘립니다.

   비피라미드형 TIFF를 제공하는 이미지의 경우 [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml] 구성 파일의 `MaxNonDsfSize`에 대한 속성 값을 늘립니다.

* Adobe Photoshop CS3에서는 기본적으로 합성 이미지가 포함된 레이어 PSD 파일을 저장하지 않습니다.

   *증상*:

   Adobe Photoshop CS3 레이어로 구성된 PSD 파일은 &quot;이 레이어로 구성된 Photoshop 파일은 합성 이미지와 함께 저장되지 않았습니다.&quot;라는 텍스트가 포함된 검정색으로 표시됩니다. 을 채우는 것이 좋습니다.

   *해결 방법*:

   호환성을 최대화하여 Adobe Photoshop CS3 파일을 저장합니다.

* CMYK/JPEG 응답 이미지에 ICC 프로필을 지정하면 일부 브라우저에서 색상이 반전됩니다.*작업 영역*:

   `fmt=`을(를) 사용하여 응답 이미지 형식 변경

* 파일 헤더를 포함하여 HTTP 응답 이미지 데이터 후 압축의 크기는 16MB로 제한됩니다.
* &quot;..&quot; 은 HTTP 요청의 경로 요소에서는 허용되지 않습니다.
* 제거 시 *[!DNL install_root]* 또는 하위 폴더에서 사용자가 만들거나 수정한 파일을 제거할 수 있습니다. 제거하기 전에 해당 파일을 다른 위치에 복사합니다.

## {#section-b08ad535e4454265b8157dec244c4faf} 이미지 제공에만 적용되는 제한 사항

* RTF( `\cf`) 명령의 전경색은 PhotoFont 텍스트에 대해 지원되지 않습니다.
* 굵게, 기울임체 및 굵은/기울임체 합성이 PhotoFont 텍스트에 대한 오류로 거부됩니다.
* PhotoFont 텍스트에는 세로 텍스트 흐름이 지원되지 않습니다.
* 16bpc PNG 이미지는 PhotoFont 텍스트에 지원되지 않습니다.
* 포함된 색상 프로파일이 있는 PNG 이미지에 대한 색상 교정은 하드 코딩된 옵션을 사용합니다. 렌더링 의도는 상대 색도입니다. PhotoFont 텍스트에 대해서는 검은 점 보정이 설정됩니다.
* 회사 [!DNL ini] 파일에서 로케일 번역이 활성화되면 파일 기반 조회가 지원되지 않습니다.
* 이미지 제공 기능이 닫히지 않은 Photoshop 경로를 올바르게 쓰지 않습니다.
* 이미지 제공에서는 현재 Adobe Media Encoder 4.0.1 또는 이전 버전을 사용하여 내보낸 TIFF 파일의 처리를 지원하지 않습니다. Adobe Media Encoder은 Premiere Pro CS4, After Effects CS4 및 Creative Suite 4 Production Premium에 포함되어 있습니다.
* 자체 크기 레이어와 함께 `text=`을 사용하는 경우 행 정렬에 둘 이상의 설정을 사용하는 RTF 문자열을 지원하지 않습니다.

   *예*

   RTF 문자열은 자체 크기 텍스트 레이어에 대해 왼쪽 및 오른쪽 줄 정렬을 모두 사용할 수 없습니다.

* SVG에는 SVG 파일에 포함되지 않은 참조된 글꼴의 글꼴 조회 경로에 대한 자체 속성이 있습니다.

   *증상*

   글꼴 정의가 포함된 렌더링된 SVG 이미지가 잘못된 글꼴을 사용하고 있습니다.

   *해결 방법*

   [!DNL install_root/ImageServing/conf/PlatformServer.conf]에서 `svgProvider.fontRoot=` 속성을 설정합니다.

* 자르기는 현재 새로 확장된 영역을 채우기 위해 `color=` 대신 `bgColor=`을 사용하고 있습니다.

* `bgColor=`이(가) 색상 프로필과 관련된 기본 색상 공간과 일치하지 않으면 색상 변환이 올바르지 않을 수 있습니다.
* 레이어에 마스크 또는 알파 데이터가 없는 경우 외부 레이어 효과는 렌더링되지 않습니다.

## 이미지 렌더링에만 적용 가능한 제한 사항 {#section-4c6949e797174607a3d1ab4d3d4a725a}

* 디캘과 벽 재료는 분리되지 않는다.
* 텍스처의 크기는 비네팅 보기의 크기에 따라 제한됩니다. 드문 경우이지만, 보기 크기의 기본 제한인 425%는 매우 큰 비반복 가능한 텍스처를 사용하는 응용 프로그램을 방해할 수 있습니다. 사전 정의된 제한 범위에서 애플리케이션 또는 컨텐츠를 변경할 수 없는 경우 백분율을 다음과 같이 늘릴 수 있습니다. 텍스트 편집기를 사용하여 [!DNL install_root/ImageServing/conf/ImageServerRegistry.xml]을 열고 `IrMaxTextureSizeFactor`을 찾아 새 백분율 값을 입력합니다. 이미지 서버를 다시 시작하지 않고 변경 사항이 즉시 적용됩니다.

* nocache 헤더가 설정된 경우에도 Netscape 및 Opera의 JavaScript 엔진은 응답 데이터를 캐시합니다. 이로 인해 상태 저장 요청의 적절한 기능이 작동하지 않습니다.

   *해결 방법*

   타임스탬프 또는 다른 고유 식별자를 요청 문자열에 추가합니다(예: `"&.ts=currentTime`).

## {#section-906a6b2378154b3da122b2332983f7a5} 유틸리티에만 적용되는 제한 사항

`ImageConvert`때로,  `control-c`
