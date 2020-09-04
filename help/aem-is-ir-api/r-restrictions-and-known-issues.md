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

* 줄 수는 텍스트 입력의 `\copyfitmaxlines` 설정 최대값과 명시적 줄 수를 초과하지 않습니다.
* 이미지 세트에는 중괄호 및 괄호가 일치해야 합니다. 중괄호와 괄호가 일치하지 않으면 URL로 인코딩되어야 합니다.
* 서버측 글로벌 응답 시간 경고에는 오류 응답이 포함됩니다.
* 현재 이 `id=` 명령은 이미지 또는 마스크 요청과 함께 `rect=` 명령을 사용할 때 필요합니다.

## 알려진 차이점 textPs= vs text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* 합성 이탤릭체는 사용할 때보다 기울어진 부분이 덜 렌더링됩니다 `text=`.
* 밑줄은 사용 시보다 약간 작고 얇습니다 `text=`.
* `\expnd` 및 `\expndtw` 음수 값이 높으면 사용할 때 문자가 서로 앞에 배치됩니다 `text=`.

* `\charscaley` 사용 시 크기 `text=` 가 다르게 조정되지만 선 높이에 영향을 주지 않습니다.

* 텍스트의 마지막 줄이 맞지 않으면 잘라내기로 표시되는 대신 전체 줄이 삭제됩니다.
* `\slmult` 그리고 MS Word 및 `\sl` `text=`와 다르게 동작하면 현재 및 이후 단락에 적용됩니다.

* `\sb` 는 MS Word의 첫 번째 단락에 적용되며, Adobe InDesign과 Photoshop `text=`는 이를 수행하지 않습니다.

* `\sa` 는 MS Word 및 Adobe InDesign과 Photoshop 모두에 대해 마지막 단락에 적용되며 `text=`이렇게 하지 않습니다.

## 이전 버전과의 호환성 {#section-a76842f751944f4fb664af296d064122}

* RTF 문자열에서 밑줄 문자( `\_`)를 이스케이프 처리하는 것은 `textPs=`

* 대/소문자를 구분하지 않는 매크로 처리를 지원합니다.
* 카탈로그 캐시가 60초에서 10초로 줄었습니다.
* 이제 오류 리디렉션 기능은 손상된 이미지, 글꼴, 색상 프로필 및 카탈로그에 게시되지만 디스크에서 찾을 수 없는 이미지를 참조하는 요청만 리디렉션합니다.
* `posN=`, `anchor=`, `anchorN=`, `origin=`및 `originN=` 이제 수정자 값이 2147483648보다 큰 경우 구문 분석 오류를 반환합니다.

* 중첩 요청의 인코딩은 지원되지 않습니다. 새 동작으로 전환하고 사이트 및 회사 카탈로그의 URL 요청에 있는 중첩 요청 값을 인코딩하지 않습니다.
* 이제 DefaultImage를 사용하면 축소판 속성이 적용됩니다 `req=tmb`.
* 이전 버전에서 `flip=`는 기준점이 무엇이든지 이미지를 다시 배치하지 않았습니다.

## 타사 라이브러리에 적용되는 제한 사항 {#section-79768b96bf634e44ab672c5b893f343d}

Digimarc 라이브러리는 Digimarc 워터마크가 이미 감지된 경우 이미지에 적용되지 않습니다. 기본 이미지를 충분히 편집하는 경우에도 Digimarc 라이브러리가 워터마크가 적용되었음을 인식할 수 있습니다. 그러나 해당 정보를 읽을 수 없을 수도 있습니다. 이렇게 하면 원본 이미지에 적용된 원본 Digimarc 정보를 가져올 수 없는 새 이미지가 만들어집니다. 이제 이미지 제공에서 회사 카탈로그에 정의된 Digimarc 워터마크를 적용할 수 있습니다.

## 이미지 제공 및 이미지 렌더링 모두에 적용되는 제한 사항 {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* Image Serving and Image Rendering may not take full advantage of all CPU when more than 4 CPU are available. 이러한 시스템의 트래픽을 시뮬레이션하여 4개 이상의 CPU에서 얼마나 유용한지 확인할 수 있습니다.
* 리디렉션(HTTP 상태 301, 302 또는 303)을 반환하는 원격 URL이 거부됩니다.
* 이 속성 `errorRedirect.rootUrl` 에 정의된 IP 주소를 구성할 때는 해당 서버의 규칙 세트 `<addressfilter>` 태그 값에 포함되어야 합니다.

   *예*:

   서버 A가 정의되었습니다 `errorRedirect.rootUrl=10.10.10.10` .

   IP 주소가 10.10.10.10인 서버 B는 규칙 세트 파일에 `<addressfilter>` 태그 값을 설정하여 해당 IP 주소(10.10.10.10)를 포함합니다.

* 위치가 지정된 점 텍스트 및 텍스트 패스는 클리핑될 수 있습니다.
* `text=` 단락 `\sa` 이 아닌 전체 텍스트 블록에만 `\sb` 적용됩니다.

* URL에 정의된 회사 및 `src=` 또는 `mask=` 수정자에 대해 정의된 다른 회사를 사용하는 경우, 이 작업 요청 양식을 위해 정의된 회사 `src=` 에 슬래시(/) `mask=` 를 붙여야 합니다.

   *예*:

   `/is/image/MyCompany?src=/YourCompany/MyImage` .

   대신: `/is/image/MyCompany?src=YourCompany/MyImage` .

* 비피라미드형 Tiff 또는 비네팅 요청은

   *&quot;이미지`C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt`에 유효한 DSF가 없으며 2.25MPixel이 최대 2MPixel을 초과합니다&quot;* .

   피라미드 스티프와 비네팅을 사용하는 것이 좋습니다. 비피라미드형 또는 비네팅을 사용해야 하는 경우 아래 지침에 따라 크기 제한을 늘리십시오.

   *작업 영역*:

   비피라미드가 아닌 이미지 렌더링의 경우 구성 파일의 IrMaxNonPyrVignetteSize 속성 값을 [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml] 높입니다.

   이미지 제공 비피라미드형 TIFF의 경우 구성 파일 `MaxNonDsfSize` 의 속성 값을 [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml] 높입니다.

* Adobe Photoshop CS3에서는 기본적으로 복합 이미지로 레이어로 구성된 PSD 파일을 저장하지 않습니다.

   *증상*:

   Adobe Photoshop CS3 레이어로 구성된 PSD 파일은 &quot;이 레이어로 구성된 Photoshop 파일은 합성 이미지와 함께 저장되지 않았습니다.&quot;라는 텍스트가 포함된 검정색으로 표시됩니다. for the Image Serving reply image or in IPS.

   *해결 방법*:

   호환성을 최대화하여 Adobe Photoshop CS3 파일을 저장합니다.

* CMYK/JPEG 회신 이미지에 ICC 프로필을 지정하면 일부 브라우저에서 색상이 반전됩니다.*작업 영역*:

   회신 이미지 형식 변경 `fmt=`

* 파일 헤더를 포함하여 HTTP 응답 이미지 데이터 후 압축의 크기는 16MB로 제한됩니다.
* &quot; ..&quot; 은 HTTP 요청의 경로 요소에서는 허용되지 않습니다.
* 제거 시 사용자 생성 또는 수정된 파일을 *[!DNL install_root]* 또는 하위 폴더에서 제거할 수 있습니다. 제거하기 전에 해당 파일을 다른 위치에 복사합니다.

## 이미지 서비스에만 적용되는 제한 사항 {#section-b08ad535e4454265b8157dec244c4faf}

* RTF() 명령의 전경 색상은 PhotoFont 텍스트에 `\cf`지원되지 않습니다.
* 굵게, 기울임꼴 및 굵은 기울임체 합성이 PhotoFont 텍스트에 대한 오류로 거부됩니다.
* PhotoFont 텍스트에는 세로 텍스트 흐름이 지원되지 않습니다.
* 16bpc PNG 이미지는 PhotoFont 텍스트에 지원되지 않습니다.
* 포함된 색상 프로파일을 포함한 PNG 이미지의 색상 교정은 하드 코딩된 옵션을 사용합니다. 렌더링 의도는 상대 색도이지만 PhotoFont 텍스트에 대해서는 검은 점 보정 기능이 설정됩니다.
* 회사 [!DNL ini] 파일에서 로케일 변환이 활성화된 경우 파일 기반 조회는 지원되지 않습니다.
* 이미지 제공 기능이 닫히지 않은 Photoshop 경로를 올바르게 쓰지 않습니다.
* 현재 이미지 제공에서는 Adobe Media Encoder 4.0.1 이전 버전을 사용하여 내보낸 TIFF 파일의 처리를 지원하지 않습니다. Adobe Media Encoder은 Premiere Pro CS4, After Effects CS4 및 Creative Suite 4 Production Premium에 포함되어 있습니다.
* 자체 크기 레이어 `text=` 와 함께 사용하면 줄 맞춤을 위해 두 개 이상의 설정을 사용하는 RTF 문자열을 지원하지 않습니다.

   *예*

   RTF 문자열은 자체 크기 텍스트 레이어에 대해 왼쪽 및 오른쪽 줄 맞춤을 모두 사용할 수 없습니다.

* SVG에는 SVG 파일에 포함되지 않은 참조된 글꼴의 글꼴 조회 경로에 대한 자체 속성이 있습니다.

   *증상*

   글꼴 정의가 포함된 렌더링된 SVG 이미지가 잘못된 글꼴을 사용하고 있습니다.

   *해결 방법*

   속성을 `svgProvider.fontRoot=` 로 설정합니다 [!DNL install_root/ImageServing/conf/PlatformServer.conf] .

* 자르기는 현재 새로 확장된 영역을 채우는 `bgColor=` 대신 `color=` 사용됩니다.

* 색상 프로파일과 관련된 기본 색상 공간과 일치하지 않는 경우 색상 변환이 정확하지 않을 수 `bgColor=` 있습니다.
* 레이어에 마스크 또는 알파 데이터가 없는 경우 외부 레이어 효과는 렌더링되지 않습니다.

## 이미지 렌더링에만 적용되는 제한 사항 {#section-4c6949e797174607a3d1ab4d3d4a725a}

* 디칼스 및 벽 재료는 분리되지 않습니다.
* 텍스처의 크기는 비네팅 보기의 크기에 비례하여 제한됩니다. 드문 경우이지만, 기본 보기 크기 425%가 반복되는 크기가 매우 큰 텍스처를 사용하여 애플리케이션을 방해할 수 있습니다. 사전 정의된 제한 범위에서 애플리케이션 또는 컨텐츠를 변경할 수 없는 경우 비율을 다음과 같이 늘릴 수 있습니다. 텍스트 편집기를 사용하여 열고 [!DNL install_root/ImageServing/conf/ImageServerRegistry.xml]찾은 다음 새로운 백분율 값 `IrMaxTextureSizeFactor` 을 입력합니다. 이미지 서버를 다시 시작하지 않고 변경 사항이 즉시 적용됩니다.

* nocache 헤더가 설정된 경우에도 Netscape 및 Opera의 JavaScript 엔진은 캐시 응답 데이터를 캐시합니다. 이로 인해 상태 저장 요청의 적절한 기능이 작동하지 않습니다.

   *해결 방법*

   타임스탬프나 다른 고유 식별자를 요청 문자열에 추가합니다(예: `"&.ts=currentTime`).

## 유틸리티에만 적용되는 제한 사항 {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`때때로 한 번의 클릭으로 중지될 때 세그멘테이션 오류가 발생합니다 `control-c`.
