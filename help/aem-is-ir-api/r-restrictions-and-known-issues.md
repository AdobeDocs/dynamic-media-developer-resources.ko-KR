---
description: Scene7 이미지 제공 사용 시 고려해야 하는 몇 가지 제한 사항과 알려진 문제가 있습니다.
seo-description: Scene7 이미지 제공 사용 시 고려해야 하는 몇 가지 제한 사항과 알려진 문제가 있습니다.
seo-title: 제한 및 알려진 문제
solution: Experience Manager
title: 제한 및 알려진 문제
topic: Scene7 Image Serving - Image Rendering API
uuid: 9f9fad41-4828-4fba-8f5f-2c33e7811c71
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 제한 및 알려진 문제{#restrictions-and-known-issues}

Scene7 이미지 제공 사용 시 고려해야 하는 몇 가지 제한 사항과 알려진 문제가 있습니다.

## 설명서 오류 {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* 줄 수는 텍스트 입력의 최대 `\copyfitmaxlines` 설정과 명시적 줄 수를 초과하지 않습니다.
* 이미지 세트에는 중괄호 및 괄호가 일치해야 합니다. 중괄호와 괄호가 일치하지 않으면 URL로 인코딩해야 합니다.
* 서버측 글로벌 응답 시간 경고에는 오류 응답이 포함됩니다.
* 이미지 또는 마스크 요청과 함께 `id=` `rect=` 명령을 사용할 때는 현재 명령이 필요합니다.

## 알려진 차이점 textPs= vs text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* 합성 이탤릭체는 사용할 때보다 기울어진 부분이 덜 렌더링됩니다 `text=`.
* 밑줄은 사용할 때보다 약간 더 작고 얇습니다 `text=`.
* `\expnd` 그리고 음수 값이 높은 `\expndtw` 값으로 사용하면 사용할 때 문자가 서로 앞에 배치됩니다 `text=`.

* `\charscaley` 사용할 때와 다르게 `text=` 크기가 조절되지만 선 높이에는 영향을 주지 않습니다.

* 텍스트의 마지막 줄이 맞지 않으면 잘라내기로 표시되는 대신 전체 줄이 삭제됩니다.
* `\slmult` MS Word 및 MS Word와 다르게 `\sl` 동작하면 현재 및 이후 단락에 대해 `text=`적용됩니다.

* `\sb` MS Word의 첫 번째 단락에 적용되며 Adobe InDesign과 Photoshop `text=`에서는 이 작업을 수행하지 않습니다.

* `\sa` MS Word의 마지막 단락에 적용되며 Adobe InDesign과 Photoshop `text=`에서는 이 작업을 수행하지 않습니다.

## 이전 버전과의 호환성 {#section-a76842f751944f4fb664af296d064122}

* RTF 문자열에서 밑줄 문자( `\_`)를 이스케이프해도 `textPs=`

* 대/소문자를 구분하지 않는 매크로 처리를 지원합니다.
* 카탈로그 캐시가 60초에서 10초로 줄었습니다.
* 이제 오류 리디렉션 기능은 손상된 이미지, 글꼴, 색상 프로필 및 카탈로그에 게시되지만 디스크에서 찾을 수 없는 이미지를 참조하는 요청만 리디렉션합니다.
* `posN=`, `anchor=`, `anchorN=`, `origin=`and `originN=` now return a parsing error if any of the modifier values are 2147483648.

* 중첩 요청의 인코딩은 지원되지 않습니다. 새 동작으로 전환하고 사이트 및 회사 카탈로그의 URL 요청에 있는 중첩 요청 값을 인코딩하지 않습니다.
* 이제 DefaultImage를 사용할 때 축소판 속성이 적용됩니다 `req=tmb`.
* 이전 버전에서는 `flip=`앵커 포인트의 위치에 관계없이 이미지가 다시 배치되지 않았습니다.

## 타사 라이브러리에 적용되는 제한 사항 {#section-79768b96bf634e44ab672c5b893f343d}

Digimarc 라이브러리가 이미 감지된 경우 이미지에 Digimarc 워터마크를 적용하기를 거부합니다. 마스터 이미지를 충분히 편집하는 경우 Digimarc 라이브러리가 워터마크가 적용되었음을 인식할 수 있습니다. 그러나 해당 정보를 읽을 수 없을 수도 있습니다. 이렇게 하면 원본 이미지에 적용된 원본 Digimarc 정보를 가져올 수 없는 새 이미지가 만들어집니다. 이제 이미지 제공에서 회사 카탈로그에 정의된 Digimarc 워터마크를 적용할 수 있습니다.

## 이미지 제공 및 이미지 렌더링 모두에 적용되는 제한 사항 {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* Image Serving and Image Rendering may not take full advantage of all CPU when more than 4 CPU are available. 이러한 시스템에서 트래픽을 시뮬레이션하여 4개 이상의 CPU를 사용하여 얼마나 편리한지를 확인할 수 있습니다.
* 리디렉션(HTTP 상태 301, 302 또는 303)을 반환하는 원격 URL이 거부됩니다.
* 이 속성에 `errorRedirect.rootUrl` 정의된 IP 주소를 구성할 때 해당 서버의 규칙 세트 `<addressfilter>` 태그 값에 포함되어야 합니다.

   *예*:

   서버 A가 `errorRedirect.rootUrl=10.10.10.10` 정의되었습니다.

   IP 주소가 10.10.10.10인 서버 B는 규칙 세트 파일에 `<addressfilter>` 태그 값을 설정하여 IP 주소(10.10.10.10)를 포함합니다.

* 위치를 지정할 때 점 텍스트와 텍스트 패스에 클리핑이 표시될 수 있습니다.
* `text=` 단락이 아닌 전체 텍스트 블록에만 `\sa` `\sb` 적용됩니다.

* URL에 정의된 회사와 `src=` 또는 `mask=` 수정자에 대해 정의된 다른 회사를 사용하는 경우, 이 작업 요청 양식에 대해 정의된 회사에 슬래시(/)를 접두사로 붙여야 `src=` `mask=` 합니다.

   *예*:

   `/is/image/MyCompany?src=/YourCompany/MyImage` .

   대신: `/is/image/MyCompany?src=YourCompany/MyImage` 을 클릭합니다.

* 비피라미드형 Tiff 또는 비네팅 요청은

   *&quot;이미지 C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt에 유효한 DSF가 없으며 2.25MPixel 영역이 최대 2MPixel을 초과합니다&quot;* .

   가장 좋은 방법은 피라미드 스티프와 비네팅을 사용하는 것입니다. 비피라미드형 또는 비네팅을 사용해야 하는 경우 아래 지침에 따라 크기 제한을 늘리십시오.

   *작업 영역*:

   비네팅이 아닌 이미지 렌더링의 경우 [!DNL/ImageServing/bin/ImageServerRegistry.xml] 구성 파일에서 IrMaxNonPyrVignetteSize의 속성 값을 *[!DNL install_root]*&#x200B;늘립니다.

   비피라미드형 TIFF 이미지 제공의 경우 [!DNL /ImageServing/bin/ImageServerRegistry.xml] 구성 `MaxNonDsfSize` *[!DNL install_root]* 파일의 속성 값을 늘립니다.

* Adobe Photoshop CS3는 기본적으로 합성 이미지를 사용하여 레이어가 있는 PSD 파일을 저장하지 않습니다.

   *증상*:

   Adobe Photoshop CS3 레이어로 구성된 PSD 파일은 &quot;이 레이어로 구성된 Photoshop 파일은 합성 이미지와 함께 저장되지 않았습니다.&quot;라는 텍스트가 있는 검정색으로 표시됩니다. for the Image Serving reply image or in IPS.

   *해결 방법*:

   호환성이 최대화된 상태로 Adobe Photoshop CS3 파일을 저장합니다.

* CMYK/JPEG 응답 이미지에 ICC 프로필을 지정하면 일부 브라우저에서 색상이 반전됩니다.*작업 영역*:

   Change reply image format by using `fmt=`

* 파일 헤더를 포함한 HTTP 응답 이미지 데이터-후 압축 크기는 16MB로 제한됩니다.
* &quot; ..&quot; 는 HTTP 요청의 경로 요소에서는 허용되지 않습니다.
* 제거는 사용자가 만들거나 수정한 파일을 *[!DNL install_root]* 또는 하위 폴더에서 제거할 수 있습니다. 제거하기 전에 이러한 파일을 다른 위치에 복사합니다.

## 이미지 제공에만 적용되는 제한 사항 {#section-b08ad535e4454265b8157dec244c4faf}

* RTF( `\cf`) 명령의 전경 색상은 PhotoFont 텍스트에서 지원되지 않습니다.
* 굵게, 기울임체 및 굵은 기울임체 합성이 PhotoFont 텍스트에 대한 오류로 거부됩니다.
* PhotoFont 텍스트에는 세로 텍스트 흐름이 지원되지 않습니다.
* 16bpc PNG 이미지는 PhotoFont 텍스트에서 지원되지 않습니다.
* 임베드된 색상 프로파일을 포함한 PNG 이미지에 대한 색상 교정은 하드 코딩된 옵션을 사용합니다. 렌더링 의도는 상대 색도이며 PhotoFont 텍스트에 대해 검은 점 보정이 켜집니다.
* 회사 [!DNL ini] 파일에서 로케일 변환이 활성화된 경우 파일 기반 조회가 지원되지 않습니다.
* 이미지 제공 기능은 닫히지 않은 Photoshop 경로를 올바로 쓰지 않습니다.
* 이미지 제공에서는 현재 Adobe Media Encoder 4.0.1 이전 버전을 사용하여 내보낸 TIFF 파일의 처리를 지원하지 않습니다. Adobe Media Encoder는 Premiere Pro CS4, After Effects CS4 및 Creative Suite 4 Production Premium에 포함되어 있습니다.
* 자체 크기 레이어와 `text=` 함께 사용하면 줄 맞춤을 위해 둘 이상의 설정을 사용하는 RTF 문자열을 지원하지 않습니다.

   *예*

   RTF 문자열은 자체 크기 텍스트 레이어에 대해 왼쪽 및 오른쪽 줄 맞춤을 모두 사용할 수 없습니다.

* SVG에는 SVG 파일에 포함되지 않은 참조된 글꼴의 글꼴 조회 경로에 대한 자체 속성이 있습니다.

   *증상*

   글꼴 정의가 포함된 렌더링된 SVG 이미지가 잘못된 글꼴을 사용하고 있습니다.

   *해결 방법*

   [!DNL /ImageServing/conf/PlatformServer.conf] `svgProvider.fontRoot=` 에서 속성을 *[!DNL install_root]* 설정합니다.

* 자르기는 현재 새로 확장된 영역을 채우는 `bgColor=` 대신 `color=` 사용합니다.

* 색상 프로파일이 포함된 기본 색상 공간과 일치하지 `bgColor=` 않는 경우 색상 변환이 정확하지 않을 수 있습니다.
* 레이어에 마스크 또는 알파 데이터가 없는 경우 외부 레이어 효과는 렌더링되지 않습니다.

## 이미지 렌더링에만 적용되는 제한 사항 {#section-4c6949e797174607a3d1ab4d3d4a725a}

* 디캘과 벽 재료는 분리되지 않습니다.
* 텍스처의 크기는 비네팅 보기의 크기를 기준으로 제한됩니다. 드문 경우이지만, 보기 크기의 기본 제한 425%는 매우 큰 비반복 텍스처를 사용하여 애플리케이션을 방해할 수 있습니다. 사전 정의된 제한 내에서 애플리케이션 또는 컨텐츠를 변경할 수 없는 경우 비율을 다음과 같이 늘릴 수 있습니다. 텍스트 편집기를 사용하여 [!DNL /ImageServing/conf/ImageServerRegistry.xml] *[!DNL install_root]*&#x200B;을(를) 열고 새 백분율 값을 `IrMaxTextureSizeFactor` 찾아 입력합니다. 이미지 서버를 다시 시작하지 않고 변경 사항이 즉시 적용됩니다.

* nocache 헤더가 설정된 경우에도 Netscape 및 Opera의 JavaScript 엔진은 응답 데이터를 캐시합니다. 이로 인해 상태 저장 요청의 적절한 기능이 방해됩니다.

   *해결 방법*

   타임스탬프 또는 기타 고유 식별자를 요청 문자열에 추가합니다(예: `"&.ts=currentTime`).

## 유틸리티에만 적용되는 제한 사항 {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`경우에 따라 세그먼테이션 오류가 발생해도 `control-c`중단됩니다.
