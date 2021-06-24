---
description: Dynamic Media 이미지 제공 사용 시 고려해야 하는 몇 가지 제한 사항과 알려진 문제가 있습니다.
solution: Experience Manager
title: 제한 및 알려진 문제
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: fd32456b-9d99-4e82-a61c-2fc4d7030630
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '1235'
ht-degree: 0%

---

# 제한 및 알려진 문제{#restrictions-and-known-issues}

Dynamic Media 이미지 제공 사용 시 고려해야 하는 몇 가지 제한 사항과 알려진 문제가 있습니다.

## 설명서 오류 {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* 줄 수는 `\copyfitmaxlines` 설정의 최대값과 텍스트 입력의 명시적 줄 수를 초과할 수 없습니다.
* 이미지 세트에는 일치하는 중괄호와 괄호가 필요합니다. 중괄호와 괄호가 일치하지 않으면 URL로 인코딩되어야 합니다.
* 서버측 글로벌 응답 시간 경고에 오류 응답이 포함되어 있습니다.
* `id=` 명령은 현재 이미지 또는 마스크 요청과 함께 `rect=` 명령을 사용할 때 필요합니다.

## 알려진 차이점 textPs= 와 text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* 합성 기울임체는 `text=`을 사용할 때보다 기울어지지 않습니다.
* 밑줄은 `text=`을 사용할 때보다 약간 낮고 얇습니다.
* `\expnd` 및  `\expndtw` 가 음수 값과 함께 사용되면 사용할 때 문자가 서로 앞에 배치됩니다 `text=`.

* `\charscaley` 사용 시와는 다르게  `text=` 조정되지만 선 높이는 영향을 주지 않습니다.

* 마지막 텍스트 행이 맞지 않으면 컷으로 표시되지 않고 전체 줄이 삭제됩니다.
* `\slmult` 그리고  `\sl` MS Word와 다르게  `text=`동작하며 현재 및 이후의 단락에 적용됩니다.

* `\sb` MS Word와 Adobe InDesign의 첫 번째 단락에  `text=`적용되며 이 단락은 적용되지 않습니다.

* `\sa` MS Word 및 Adobe InDesign과 Photoshop 모두에 대한 마지막 단락에  `text=`적용되지 않습니다.

## 이전 버전과의 호환성 {#section-a76842f751944f4fb664af296d064122}

* RTF 문자열에서 밑줄 문자( `\_`)를 이스케이프하면 `textPs=`을 사용하여 모든 글꼴에서 작동하지 않습니다

* 대/소문자를 구분하지 않는 매크로 처리를 지원합니다.
* 카탈로그 캐시가 60초에서 10초로 줄었습니다.
* 이제 오류 리디렉션 기능은 손상된 이미지, 글꼴, 색상 프로필 및 카탈로그에서 게시되지만 디스크에서 찾을 수 없는 이미지를 참조하는 요청만 리디렉션합니다.
* `posN=`,  `anchor=`,  `anchorN=`,  `origin=`및  `originN=` 는 이제 수정자 값이 2147483648보다 큰 경우 구문 분석 오류를 반환합니다.

* 중첩 요청의 인코딩은 지원되지 않습니다. 새 동작으로 전환하고 사이트 및 회사 카탈로그의 URL 요청에 있는 중첩된 요청 값을 인코딩하지 않습니다.
* 이제 DefaultImage가 `req=tmb` 사용 시 축소판 속성을 적용합니다.
* 이전 버전에서 `flip=`을 사용하는 경우 앵커 포인트가 무엇인지에 관계없이 이미지가 다시 배치되지 않았습니다.

## 타사 라이브러리에 적용할 수 있는 제한 사항 {#section-79768b96bf634e44ab672c5b893f343d}

Digimarc 라이브러리에서는 Digimarc 워터마크가 이미 감지된 경우 이미지에 적용되지 않습니다. 기본 이미지에 충분한 편집이 수행된 경우 Digimarc 라이브러리에서 워터마크가 적용되었음을 인식할 수 있습니다. 그러나 해당 정보를 읽지 못할 수도 있습니다. 따라서 원본 이미지에 적용된 원본 Digimarc 정보를 가져올 수 없는 새 이미지가 만들어집니다. 이제 이미지 제공에서 회사 카탈로그에 정의된 Digimarc 워터마크를 적용할 수 있습니다.

## 이미지 제공 및 이미지 렌더링 모두에 적용할 수 있는 제한 사항 {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* 4개 이상의 CPU를 사용할 수 있는 경우 이미지 제공 및 이미지 렌더링이 모든 CPU를 사용하지 못할 수 있습니다. 이러한 시스템의 트래픽을 시뮬레이션하여 4개 이상의 CPU에 얼마나 유용한지 확인할 수 있습니다.
* 리디렉션을 반환하는 원격 URL(HTTP 상태 301, 302 또는 303)이 거부됩니다.
* `errorRedirect.rootUrl`을 구성할 때는 이 속성에 정의된 IP 주소를 해당 서버의 규칙 세트 `<addressfilter>` 태그 값에 포함해야 합니다.

   *예*:

   서버 A가 `errorRedirect.rootUrl=10.10.10.10` 을 정의했습니다.

   IP 주소가 10.10.10.10인 서버 B는 규칙 세트 파일에서 `<addressfilter>` 태그 값을 설정하여 해당 IP 주소(10.10.10.10)을 포함합니다.

* 위치가 있는 점 텍스트와 텍스트 패스는 클리핑을 나타낼 수 있습니다.
* `text=` 단락 `\sa` 이 아닌 전체 텍스트 블록 `\sb` 에 및 만 적용됩니다.

* URL에 정의된 한 회사와 `src=` 또는 `mask=` 수정자에 대해 정의된 다른 회사를 사용하는 경우 이 형식의 작업 요청을 사용하려면 `src=` 또는 `mask=`에 대해 정의된 회사에 슬래시 접두사를 붙여야 합니다.

   *예*:

   `/is/image/MyCompany?src=/YourCompany/MyImage` .

   대신:`/is/image/MyCompany?src=YourCompany/MyImage` .

* 비피라미드형 Tiff 또는 비네팅 요청은 와 유사한 오류 메시지를 생성합니다

   *&quot;이미지 `C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt` 에 유효한 DSF가 없으며 2.25MPixel의 영역이 최대 2MPixel을 초과합니다.&quot;* 

   가장 좋은 방법은 피라미드형 Tiff와 vignette를 사용하는 것입니다. 비피라미드형 tiff 또는 vignette를 사용해야 하는 경우 아래 지침에 따라 크기 제한을 늘리십시오.

   *작업*:

   이미지 렌더링 비피라미드형 비네팅의 경우 [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml] 구성 파일에서 IrMaxNonPyrVignetteSize의 속성 값을 늘립니다.

   이미지 제공 비피라미드형 TIFF의 경우 [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml] 구성 파일의 `MaxNonDsfSize`에 대한 속성 값을 늘립니다.

* Adobe Photoshop CS3에서는 기본적으로 합성 이미지에 레이어 PSD 파일을 저장하지 않습니다.

   *증상*:

   Adobe Photoshop CS3 레이어 PSD 파일은 &quot;이 레이어된 Photoshop 파일이 복합 이미지와 함께 저장되지 않았습니다&quot;라는 텍스트가 있는 검정색으로 표시됩니다. 이미지 제공 회신 이미지 또는 IPS에 대한.

   *해결 방법*:

   호환성을 최대화하면서 Adobe Photoshop CS3 파일을 저장합니다.

* ICC 프로파일을 CMYK/JPEG 회신 이미지에 지정하면 일부 브라우저에서 색상이 반전됩니다.*작업*:

   `fmt=` 을 사용하여 회신 이미지 형식을 변경합니다.

* 파일 헤더를 포함하여 압축 후 HTTP 응답 이미지 데이터의 크기는 16MB로 제한됩니다.
* &quot;..&quot; 은 HTTP 요청의 어떤 경로 요소에서도 허용되지 않습니다.
* 제거 시 *[!DNL install_root]* 또는 하위 폴더에서 사용자가 만들거나 수정한 파일을 제거할 수 있습니다. 제거하기 전에 해당 파일을 다른 위치에 복사합니다.

## 이미지 제공 기능에만 적용할 수 있는 제한 사항 {#section-b08ad535e4454265b8157dec244c4faf}

* PhotoFont 텍스트에는 RTF( `\cf`) 명령의 전경색이 지원되지 않습니다.
* 굵게, 기울임체 및 굵게/기울임체를 합성하면 PhotoFont 텍스트에 대한 오류로 거부됩니다.
* PhotoFont 텍스트에 대해 세로 텍스트 흐름이 지원되지 않습니다.
* 16bpc PNG 이미지는 PhotoFont 텍스트에 대해 지원되지 않습니다.
* 포함된 색상 프로필이 있는 PNG 이미지에 대한 색상 교정은 하드 코딩된 옵션을 사용합니다. 렌더링 의도가 상대 색조이고 PhotoFont 텍스트에 대해 블랙포인트 보상이 설정됩니다.
* 회사 [!DNL ini] 파일에서 로케일 변환이 활성화된 경우 파일 기반 조회는 지원되지 않습니다.
* 이미지 제공 기능이 닫히지 않은 Photoshop 경로를 올바르게 쓰지 않습니다.
* 이미지 제공 서비스는 현재 Adobe Media Encoder 4.0.1 이전 버전을 사용하여 내보낸 TIFF 파일 처리를 지원하지 않습니다. Adobe Media Encoder은 Premiere Pro CS4, After Effects CS4 및 Creative Suite 4 Production Premium에 포함되어 있습니다.
* 자체 크기 조정 레이어와 함께 `text=`을 사용하면 선 맞춤에 둘 이상의 설정을 사용하는 RTF 문자열을 지원하지 않습니다.

   *예*

   RTF 문자열은 자체 크기 텍스트 레이어에 대해 왼쪽 및 오른쪽 줄 맞춤을 모두 사용할 수 없습니다.

* SVG에는 SVG 파일에 포함되지 않은 참조된 글꼴의 글꼴 조회 경로에 대한 자체 속성이 있습니다.

   *증상*

   글꼴 정의를 포함하는 렌더링된 SVG 이미지에서 잘못된 글꼴을 사용하고 있습니다.

   *해결 방법*

   [!DNL install_root/ImageServing/conf/PlatformServer.conf]에서 `svgProvider.fontRoot=` 속성을 설정합니다.

* 현재 자르기는 새로 확장된 영역을 채우기 위해 `color=` 대신 `bgColor=`을 사용하고 있습니다.

* `bgColor=`이(가) 색상 프로필과 관련된 기본 색상 공간과 일치하지 않으면 색상 변환이 올바르지 않을 수 있습니다.
* 레이어에 마스크나 알파 데이터가 없으면 외부 레이어 효과가 렌더링되지 않습니다.

## 이미지 렌더링에만 적용할 수 있는 제한 사항 {#section-4c6949e797174607a3d1ab4d3d4a725a}

* 디칼과 벽체는 탈착할 수 없다.
* 텍스처의 크기는 비네팅 보기의 크기에 따라 제한됩니다. 드문 경우이지만, 보기 크기의 기본 제한인 425%가 매우 큰 비반복 가능한 텍스처를 사용하여 응용 프로그램을 방해할 수 있습니다. 사전 정의된 제한 내에서 응용 프로그램 또는 콘텐츠를 변경할 수 없는 경우 백분율을 다음과 같이 높일 수 있습니다. 텍스트 편집기를 사용하여 [!DNL install_root/ImageServing/conf/ImageServerRegistry.xml] 을 열고 `IrMaxTextureSizeFactor` 를 찾은 다음 새 백분율 값을 입력합니다. 변경 사항은 이미지 서버를 다시 시작하지 않고 즉시 적용됩니다.

* nocache 헤더가 설정된 경우에도 Netscape 및 Opera 캐시 응답 데이터의 JavaScript 엔진입니다. 이로 인해 상태 저장 요청의 적절한 기능이 작동하지 않습니다.

   *해결 방법*

   타임스탬프나 다른 고유 식별자를 요청 문자열(예: `"&.ts=currentTime`)에 추가합니다.

## 유틸리티에만 적용되는 제한 사항 {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`를 사용하여 중지하면 세그먼트 문제로 가끔  `control-c`충돌합니다.
