---
description: 이미지 렌더링은 ICC(International Color Consortium) 사양을 준수하는 색상 공간 프로파일을 기반으로 색상 공간 변환을 지원합니다.
seo-description: 이미지 렌더링은 ICC(International Color Consortium) 사양을 준수하는 색상 공간 프로파일을 기반으로 색상 공간 변환을 지원합니다.
seo-title: 이미지 렌더링 색상 관리 *
solution: Experience Manager
title: 이미지 렌더링 색상 관리 *
topic: Scene7 Image Serving - Image Rendering API
uuid: 9c47f584-645f-4eb7-bdc0-fdef459da3b2
translation-type: tm+mt
source-git-commit: b27327f940202b1883a654702aa386c7ae83c856
workflow-type: tm+mt
source-wordcount: '761'
ht-degree: 0%

---


# 이미지 렌더링 색상 관리 *{#image-rendering-color-management}

이미지 렌더링은 ICC(International Color Consortium) 사양을 준수하는 색상 공간 프로파일을 기반으로 색상 공간 변환을 지원합니다.

**제한 사항**

현재 CMYK, RGB 및 회색 크기 조절 색상 공간만 지원됩니다.

캐비닛 스타일 파일(.vnc) 및 윈도우 커버 스타일 파일( [!DNL .vnw])은 색상 관리가 되지 않으며 작업 색상 공간에 존재하는 것으로 가정합니다.

**참조**

[International Color Consortium](http://www.color.org/index.xalter) ,  [ `icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06) ,  [ `iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f) ,  `attribute::IccProfile*`  `attribute::IccProfileSrc*`,  `attribute::IccRenderIntent`  `attribute::IccBlackPointCompensation`   `attribute::IccDither` ,, ICC 프로파일 맵

## 기본 색상 공간 {#section-8ce27edf42e746febe4654f8f19b9c0c}

각 이미지 카탈로그(및 기본 카탈로그)는 ICC 프로파일 세트를 정의할 수 있습니다. 이러한 프로필은 이 카탈로그에 대한 기본 색상 공간을 구성합니다. 회색 음영, RGB 및 CMYK 데이터( `attribute::IccProfileRgb`, `attribute::IccProfileGray`, `attribute::IccProfileCmyk`, `attribute::IccProfileSrcRgb`, `attribute::IccProfileSrcGray` 및 `attribute::IccProfileSrcCmyk`)에 대해 각각 하나의 입력 및 하나의 출력 프로필입니다.

이미지의 픽셀 유형에 따라 카탈로그 기본 프로필에서 특정 이미지 또는 다른 개체의 기본 색상 공간이 선택됩니다.

## 입력 색상 공간 {#section-660f661a7e954df4b451e34134195276}

재료 이미지는 입력 색상 공간을 정의하기 위해 ICC 프로파일을 포함할 수 있습니다. 소스 이미지에 프로필이 포함되지 않은 경우 소스 이미지의 픽셀 유형에 해당하는 해당 이미지 카탈로그의 `attribute::IccProfileSrc*`이(가) 사용됩니다. 이미지 카탈로그에 이 속성이 정의되지 않은 경우 `attribute::IccProfile*`이(가) 사용됩니다. 해당 카탈로그 속성이 정의되지 않은 경우 이미지는 색상 관리가 되지 않으며 기본 변환만 적용됩니다.

## 작업 중인 색상 공간 {#section-645d9cfa5b0347a190a0ece218f5b5e1}

일반적으로 작업 색상 공간은 비네팅에 포함된 ICC 색상 프로파일에 의해 정의됩니다. 비네팅에 프로파일이 없는 경우 작업 색상 공간에 기본 RGB 입력 프로파일(`attribute::IccProfileSrcRgb` 세션 카탈로그의 기본 RGB 입력 프로파일)이 사용됩니다.

모든 렌더링 작업은 작업 색상 공간에서 실행됩니다.

**중요:** 작업 색상 공간에 대한 ICC 프로필은 입력 및 출력 변형을 지원해야 합니다. 출력 전용 프로파일이 작업 색상 공간으로 사용되는 경우 AIR에서는 자료를 해당 영역으로 변환할 수 없습니다. 동일한 작업 색상 공간에 자료가 있는 경우에도 이러한 색상 프로파일을 사용할 수 있습니다. 다른 색상 공간에 재질을 적용하려고 하면 실패합니다.

## 명시적 색상 값 {#section-31727bf1b23e477ca92572fbbf422d2f}

`color=`, `bgc=`, `catalog::BgColor` 및 `catalog::Color`에 지정된 RGB 색상 값이 현재 작업 색상 공간에 있는 것으로 가정합니다.

## 자료 데이터 파일 {#section-33f7a170a6664c02b8479fb89cc0aea3}

질감 이미지 파일(텍스처 및 decal 이미지)은 RGB, 회색 음영 또는 CMYK 픽셀 유형을 가질 수 있으며 색상 프로파일을 포함할 수 있습니다. 색상 프로파일이 포함되지 않은 경우 기본 입력 색상 공간은 이미지와 연결됩니다(예: 이미지의 픽셀 유형에 해당하는 재료 카탈로그의 색상 프로파일).

중첩된 이미지 제공 또는 이미지 렌더링 요청에서 얻은 자료 이미지에는 일반적으로 색상 프로필이 포함됩니다. 이 경우 이미지는 픽셀 유형에 해당하는 기본 입력 색상 공간과 연결됩니다.

이미지 파일의 색상 공간이 작업 색상 공간과 다른 경우 정확한 색상 변환을 사용하여 작업 색상 공간으로 변환할 수 있습니다. 기본 유형 변환은 프로파일이 포함되지 않고 기본 입력 프로파일이 정의되지 않은 경우에 사용됩니다.

캐비닛 스타일 파일( [!DNL .vnc]) 또는 파일을 덮는 창( [!DNL .vnw])과 같은 다른 자료 데이터 파일은 색상 프로파일을 포함하지 않으며 항상 작업 색상 공간에 있는 것으로 가정합니다.

## 출력 색상 공간 {#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

모든 렌더링 작업은 작업 색상 공간에서 수행됩니다. 요청에서 `icc=` 명령을 사용하여 다른 색상 프로파일을 지정하면 데이터가 인코딩되어 클라이언트로 반환되기 직전에 해당 색상 공간으로 변환됩니다. 색상 관리가 비활성화된 경우 회색 음영 또는 CMYK로 변환해야 하는 경우 자동 변환이 사용됩니다.

## 포함된 색상 프로필 {#section-5ff733832d38429fbe02b3c1e9bb94a9}

요청에 대해 `iccEmbed=`을 지정하여 렌더링된 이미지와 연결된 색상 프로필을 응답 이미지에 포함할 수 있습니다.

`icc=`을(를) 지정하지 않으면 작업 색상 공간에 대한 ICC 프로필이 포함됩니다. 색상 관리가 비활성화되어 있고 `icc=`으로 지정된 프로파일이 없을 경우 프로필이 포함되지 않습니다.

## ICC 프로필 {#section-afeb76068b5042adb83261638e450140}

서버에서 사용하는 모든 색상 프로필은 ICC 사양을 준수해야 합니다. ICC 프로필 파일은 일반적으로 [!DNL .icc] 또는 [!DNL .icm] 파일 접미어를 사용하며 자료 데이터 파일과 함께 있습니다.

출력 프로필은 `icc=` 명령에서 파일 경로/이름으로 지정할 수 있지만 기본 카탈로그 또는 특정 자료 카탈로그의 ICC 프로필 맵에 있는 모든 프로필 파일을 등록하고 파일 경로 대신 단축키 식별자( `icc::Name`)를 사용하는 것이 좋습니다.

작업 프로필은 재료 카탈로그 또는 기본 카탈로그의 ICC 프로필 맵에 등록해야 합니다.
