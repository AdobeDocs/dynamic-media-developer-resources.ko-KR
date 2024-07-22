---
description: Dynamic Media 이미지 서비스 제공 을 사용할 때 고려해야 하는 몇 가지 제한 사항과 알려진 문제가 있습니다.
solution: Experience Manager
title: 제한 사항 및 알려진 문제
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd32456b-9d99-4e82-a61c-2fc4d7030630
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1235'
ht-degree: 0%

---

# 제한 사항 및 알려진 문제{#restrictions-and-known-issues}

Dynamic Media 이미지 서비스 제공 을 사용할 때 고려해야 하는 몇 가지 제한 사항과 알려진 문제가 있습니다.

## 설명서 정오표 {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* 줄 수가 `\copyfitmaxlines` 설정의 최대값과 텍스트 입력에 있는 명시적 줄 수를 초과하지 않습니다.
* 이미지 집합에 일치하는 중괄호와 괄호가 필요합니다. 중괄호와 괄호가 일치하지 않으면 URL로 인코딩해야 합니다.
* 서버측 글로벌 응답 시간 경고에 오류 응답이 포함됩니다.
* 이미지 또는 마스크 요청에 `rect=` 명령을 사용할 때는 현재 `id=` 명령이 필요합니다.

## 알려진 차이점 textPs= 와 text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* 합성 기울임꼴 은 `text=`을(를) 사용할 때보다 덜 기울어집니다.
* 밑줄은 `text=`을(를) 사용할 때보다 약간 더 낮고 얇습니다.
* 음수 값이 높은 `\expnd` 및 `\expndtw`을(를) 사용하면 `text=`을(를) 사용할 때 문자가 서로 앞에 놓입니다.

* `\charscaley`은(는) `text=`을(를) 사용할 때와 다르게 크기가 조절되지만 선 높이에는 영향을 주지 않습니다.

* 텍스트의 마지막 줄이 맞지 않으면 잘라내기로 표시되지 않고 전체 줄이 삭제됩니다.
* `\slmult`과(와) `\sl`은(는) MS Word 및 `text=`과(와) 다르게 동작하므로 현재 단락과 그 다음 단락에 적용됩니다.

* `\sb`은(는) MS Word 및 `text=`의 첫 번째 단락에 모두 적용되며, Adobe InDesign 및 [!DNL Photoshop]은(는) 적용되지 않습니다.

* `\sa`은(는) MS Word 및 `text=`의 마지막 단락에 모두 적용되며, Adobe InDesign 및 [!DNL Photoshop]은(는) 적용되지 않습니다.

## 이전 버전과의 호환성 {#section-a76842f751944f4fb664af296d064122}

* RTF 문자열의 밑줄 문자(`\_`) 이스케이프가 `textPs=`을(를) 사용하는 모든 글꼴에서 작동하지 않습니다.

* 대/소문자를 구분하지 않는 매크로 처리를 지원합니다.
* 카탈로그 캐시가 60초에서 10초로 줄었습니다.
* 이제 오류 리디렉션 기능은 카탈로그에 게시되었지만 디스크에 없는 손상된 이미지, 글꼴, 색상 프로필 및 이미지를 참조하는 요청만 리디렉션합니다.
* `posN=`, `anchor=`, `anchorN=`, `origin=` 및 `originN=`은(는) 이제 수정자 값이 2147483648보다 큰 경우 구문 분석 오류를 반환합니다.

* 중첩 요청의 인코딩은 지원되지 않습니다. 새 동작으로 전환하고 사이트의 URL 요청과 회사 카탈로그에 있는 중첩된 요청 값의 인코딩을 해제합니다.
* 이제 `req=tmb`을(를) 사용할 때 DefaultImage가 썸네일 특성을 적용합니다.
* `flip=`을(를) 사용하는 이전 버전에서는 기준점이 무엇인지에 관계없이 이미지의 위치가 변경되지 않았습니다.

## 타사 라이브러리에 적용할 수 있는 제한 사항 {#section-79768b96bf634e44ab672c5b893f343d}

Digimarc 라이브러리는 Digimarc 워터마크가 이미 감지된 경우 이미지에 Digimarc 워터마크를 적용하지 않습니다. 1차 이미지에 대해 충분히 편집한 경우 Digimarc 라이브러리는 워터마크가 적용되었음을 인식할 수 있습니다. 그러나 해당 정보를 읽지 못할 수 있습니다. 그러면 원본 이미지에 적용된 원본 Digimarc 정보를 가져올 수 없는 새 이미지가 생성됩니다. 이제 이미지 제공에서는 회사 카탈로그에 정의된 Digimarc 워터마크를 적용할 수 있습니다.

## 이미지 제공과 이미지 렌더링 모두에 적용할 수 있는 제한 사항 {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* 4개 이상의 CPU를 사용할 수 있는 경우 이미지 제공 및 이미지 렌더링이 모든 CPU를 최대한 활용하지는 못할 수 있습니다. 이 시스템의 트래픽을 시뮬레이션하여 4개 이상의 CPU에서 얼마나 유용한지 확인하십시오.
* 리디렉션을 반환하는 원격 URL(HTTP 상태 301, 302 또는 303)은 거부됩니다.
* `errorRedirect.rootUrl`을(를) 구성할 때 이 속성에 정의된 IP 주소를 해당 서버의 규칙 집합 `<addressfilter>` 태그 값에 포함해야 합니다.

  *예*:

  서버 A가 `errorRedirect.rootUrl=10.10.10.10` 을(를) 정의했습니다.

  IP 주소가 10.10.10.10인 서버 B는 규칙 세트 파일에서 `<addressfilter>` 태그 값을 설정하여 IP 주소(10.10.10.10)를 포함합니다.

* 위치 지정이 있는 점 텍스트 및 텍스트 패스는 클리핑을 나타낼 수 있습니다.
* `text=`은(는) 단락별로 적용되지 않고 전체 텍스트 블록에만 `\sa` 및 `\sb`을(를) 적용합니다.

* URL에 정의된 회사와 `src=` 또는 `mask=` 수정자에 대해 정의된 다른 회사를 사용하는 경우 이 요청 형식이 작동하도록 하려면 `src=` 또는 `mask=`에 대해 정의된 회사에 슬래시 접두사를 사용해야 합니다.

  *예*:

  `/is/image/MyCompany?src=/YourCompany/MyImage` .

  대신: `/is/image/MyCompany?src=YourCompany/MyImage`.

* 피라미드화되지 않은 Tiff 또는 비네팅 요청은에 유사한 오류 메시지를 생성합니다.

  *&quot;이미지 `C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt`에 유효한 DSF가 없으며 2.25MPixel의 면적이 최대 2MPixel&quot;*&#x200B;을(를) 초과합니다.

  가장 좋은 방법은 피라미드 Tiff와 vignette를 사용하는 것입니다. 비 피라미드형 팁이나 비네팅을 사용해야 하는 경우 아래 지침에 따라 크기 제한을 늘리십시오.

  *해결 방법*:

  이미지 렌더링 비피라미드형 비네팅의 경우 [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml] 구성 파일에서 IrMaxNonPyrVignetteSize의 속성 값을 늘립니다.

  이미지 제공 비피라미드형 TIFF의 경우 [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml] 구성 파일에서 `MaxNonDsfSize`의 속성 값을 늘리십시오.

* Adobe [!DNL Photoshop] CS3은(는) 기본적으로 합성 이미지로 계층화된 PSD 파일을 저장하지 않습니다.

  *증상*:

  Adobe [!DNL Photoshop] CS3 계층화된 PSD 파일이 &quot;이 계층화된 [!DNL Photoshop] 파일이 복합 이미지로 저장되지 않았습니다.&quot;라는 텍스트가 있는 검정색으로 표시됩니다. 이미지 제공 응답 이미지용 또는 IPS용

  *해결 방법*:

  호환성 최대화가 설정된 Adobe [!DNL Photoshop] CS3 파일을 저장합니다.

* ICC 프로파일을 CMYK/JPEG 응답 이미지에 할당하면 일부 브라우저에서 색상이 반전됩니다.*해결 방법*:

  `fmt=`을(를) 사용하여 응답 이미지 형식 변경

* 파일 헤더를 포함한 압축 후 HTTP 응답 이미지 데이터의 크기는 16MB로 제한됩니다.
* &quot; ..&quot; 은(는) HTTP 요청의 경로 요소에서 허용되지 않습니다.
* *[!DNL install_root]* 또는 하위 폴더에서 사용자가 만들거나 수정한 파일을 제거할 수 있습니다. 제거하기 전에 이러한 파일을 다른 위치에 복사합니다.

## 이미지 제공에만 적용할 수 있는 제한 사항 {#section-b08ad535e4454265b8157dec244c4faf}

* PhotoFont 텍스트에는 RTF(`\cf`) 명령의 전경색이 지원되지 않습니다.
* 굵게, 기울임체 및 굵게/기울임체 합성은 PhotoFont 텍스트에 대한 오류로 거부됩니다.
* 세로 텍스트 흐름은 PhotoFont 텍스트에 대해 지원되지 않습니다.
* PhotoFont 텍스트에는 16bpc PNG 이미지가 지원되지 않습니다.
* 색상 프로파일이 포함된 PNG 이미지의 색상을 수정하면 하드 코딩된 옵션이 사용됩니다. 렌더링 의도는 상대 색도계이며 PhotoFont 텍스트에 대해 검은 점 보상이 켜져 있습니다.
* 회사 [!DNL ini] 파일에서 로케일 변환이 활성화된 경우 파일 기반 조회가 지원되지 않습니다.
* 이미지 제공에서 닫히지 않은 [!DNL Photoshop] 경로를 올바르게 쓰지 않습니다.
* 이미지 제공은 현재 Adobe Media Encoder 4.0.1 이전 버전을 사용하여 내보낸 TIFF 파일의 처리를 지원하지 않습니다. Adobe Media Encoder은 Premiere Pro CS4, After Effects CS4 및 Creative Suite 4 Production Premium에 포함되어 있습니다.
* 자체 크기 조정 레이어와 함께 `text=`을(를) 사용하면 줄 양쪽 맞춤에 두 개 이상의 설정을 사용하는 RTF 문자열이 지원되지 않습니다.

  *예*

  RTF 문자열은 자체 크기 조정 텍스트 레이어의 왼쪽 및 오른쪽 줄 양쪽 맞춤을 모두 사용할 수 없습니다.

* SVG은 SVG 파일에 포함되지 않은 참조된 글꼴의 글꼴 조회 경로에 대한 자체 속성이 있습니다.

  *증상*

  글꼴 정의가 포함된 렌더링된 SVG 이미지에서 잘못된 글꼴을 사용하고 있습니다.

  *해결 방법*

  [!DNL install_root/ImageServing/conf/PlatformServer.conf]에서 `svgProvider.fontRoot=` 속성을 설정합니다.

* 자르기는 현재 `color=` 대신 `bgColor=`을(를) 사용하여 새로 확장된 영역을 채우는 중입니다.

* `bgColor=`이(가) 색상 프로파일을 포함하는 기본 색상 공간과 일치하지 않으면 색상 변환이 올바르지 않을 수 있습니다.
* 레이어에 마스크나 알파 데이터가 없으면 외부 레이어 효과가 렌더링되지 않습니다.

## 이미지 렌더링에만 적용할 수 있는 제한 사항 {#section-4c6949e797174607a3d1ab4d3d4a725a}

* 데칼과 벽 재질은 제거할 수 없습니다.
* 텍스처의 크기는 비네팅 뷰의 크기에 따라 제한됩니다. 드문 경우이지만, 뷰 크기의 425%라는 기본 제한은 매우 큰 반복할 수 없는 텍스처를 사용하는 애플리케이션을 방해할 수 있다. 사전 정의된 제한 사항 내에서 애플리케이션 또는 콘텐츠를 변경하여 사용할 수 없는 경우 백분율을 다음과 같이 늘릴 수 있습니다. 텍스트 편집기를 사용하여 [!DNL install_root/ImageServing/conf/ImageServerRegistry.xml]을(를) 열고 `IrMaxTextureSizeFactor`을(를) 찾은 다음 새 백분율 값을 입력하십시오. 변경 사항은 이미지 서버를 다시 시작하지 않고 즉시 적용됩니다.

* Netscape 및 Opera의 JavaScript 엔진은 nocache 헤더가 설정되어 있더라도 응답 데이터를 캐시합니다. 이로 인해 상태 저장 요청의 적절한 기능이 방해됩니다.

  *해결 방법*

  타임스탬프 또는 `"&.ts=currentTime`과 같은 다른 고유 식별자를 요청 문자열에 추가합니다.

## 유틸리티에만 적용할 수 있는 제한 사항 {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`은(는) `control-c`(으)로 중지될 때 때로 세그먼테이션 오류와 충돌합니다.
