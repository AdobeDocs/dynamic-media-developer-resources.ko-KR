---
description: 이미지 렌더링은 ICC(International Color Consortium) 사양을 준수하는 색상 공간 프로필을 기반으로 색상 공간 변환을 지원합니다.
solution: Experience Manager
title: 이미지 렌더링 색상 관리 *
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa772ab2-8a32-4c1a-9ee3-c1cf4a0b3095
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 0%

---

# 이미지 렌더링 색상 관리 *{#image-rendering-color-management}

이미지 렌더링은 ICC(International Color Consortium) 사양을 준수하는 색상 공간 프로필을 기반으로 색상 공간 변환을 지원합니다.

**제한 사항**

현재 CMYK, RGB 및 회색 음영 색상 공간만 지원됩니다.

캐비닛 스타일 파일(.vnc) 및 창 커버 스타일 파일( [!DNL .vnw])은 색상 관리가 아니며 작업 색상 공간에 존재하는 것으로 간주됩니다.

**참조**

[International Color Consortium](https://www.color.org/index.xalter) ,  [ `icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06) ,  [ `iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f) ,  `attribute::IccProfile*` ,  `attribute::IccProfileSrc*`,  `attribute::IccRenderIntent` ,  `attribute::IccBlackPointCompensation` ,  `attribute::IccDither` , ICC 프로필 맵

## 기본 색상 공간 {#section-8ce27edf42e746febe4654f8f19b9c0c}

각 이미지 카탈로그(및 기본 카탈로그)는 ICC 프로파일 집합을 정의할 수 있습니다. 이러한 프로필은 이 카탈로그의 기본 색상 공간으로서, 회색 음영, RGB 및 CMYK 데이터( `attribute::IccProfileRgb`, `attribute::IccProfileGray`, `attribute::IccProfileCmyk`, `attribute::IccProfileSrcRgb`, `attribute::IccProfileSrcGray` 및 `attribute::IccProfileSrcCmyk`)에 대해 각각 하나의 입력 및 하나의 출력 프로파일을 구성합니다.

이미지의 픽셀 유형에 따라 카탈로그 기본 프로필에서 특정 이미지나 다른 객체의 기본 색상 공간이 선택됩니다.

## 입력 색상 공간 {#section-660f661a7e954df4b451e34134195276}

재료 이미지는 ICC 프로파일을 포함하여 입력 색상 공간을 정의할 수 있습니다. 소스 이미지에 포함된 프로필이 없으면 소스 이미지의 픽셀 유형에 해당하는 적용 가능한 이미지 카탈로그의 `attribute::IccProfileSrc*`이 사용됩니다. 이 속성이 이미지 카탈로그에 정의되지 않으면 `attribute::IccProfile*`이 사용됩니다. 해당 카탈로그 속성이 정의되지 않은 경우 이미지가 색상 관리가 아니며 단순 변환만 적용됩니다.

## 작업 색상 공간 {#section-645d9cfa5b0347a190a0ece218f5b5e1}

일반적으로 작업 색상 공간은 비네트에 포함된 ICC 색상 프로파일에 의해 정의됩니다. 비네팅에 프로필이 포함되지 않으면, 작업 색상 공간에 기본 RGB 입력 프로필( 세션 카탈로그의 `attribute::IccProfileSrcRgb`)이 사용됩니다.

모든 렌더링 작업은 작업 색상 공간에서 실행됩니다.

**중요:** 작업 색상 공간의 ICC 프로파일은 입력 및 출력 변환을 지원해야 합니다. 출력 전용 프로파일을 작업 색상 공간으로 사용하는 경우 IR에서는 재료를 작업 색상 공간으로 변환할 수 없습니다. 이러한 색상 프로파일은 같은 작업 색상 공간에 소재가 존재하는 경우에도 사용할 수 있습니다. 다른 색상 공간에 재료를 적용하려고 시도해도 실패합니다.

## 명시적 색상 값 {#section-31727bf1b23e477ca92572fbbf422d2f}

`color=`, `bgc=`, `catalog::BgColor` 및 `catalog::Color`에 지정된 RGB 색상 값은 현재 작업 색상 공간에 존재하는 것으로 간주됩니다.

## 자료 데이터 파일 {#section-33f7a170a6664c02b8479fb89cc0aea3}

재료 이미지 파일(텍스쳐 및 디칼 이미지)은 RGB, 회색 크기 또는 CMYK 픽셀 유형을 가질 수 있으며 색상 프로파일을 포함할 수 있습니다. 색상 프로파일이 포함되지 않으면 기본 입력 색상 공간이 이미지와 연관됩니다(예: 이미지의 픽셀 유형에 해당하는 재료 카탈로그의 색상 프로파일).

중첩된 이미지 제공 또는 이미지 렌더링 요청에서 가져온 자료 이미지에는 일반적으로 색상 프로필이 포함됩니다. 이 경우 이미지는 픽셀 유형에 해당하는 기본 입력 색상 공간과 연결됩니다.

이미지 파일의 색상 공간이 작업 색상 공간과 다른 경우 정확한 색상 변환으로 작업 색상 공간으로 변환할 수 있습니다. 프로필이 포함되지 않고 기본 입력 프로필이 정의되지 않은 경우 단순 유형 전환이 사용됩니다.

캐비닛 스타일 파일( [!DNL .vnc]) 또는 창 커버 파일( [!DNL .vnw])과 같은 기타 자료 데이터 파일은 색상 프로파일을 포함하지 않으며 항상 작업 색상 공간에 있다고 가정합니다.

## 출력 색상 공간 {#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

모든 렌더링 작업은 작업 색상 공간에서 수행됩니다. 요청이 `icc=` 명령을 사용하여 다른 색상 프로필을 지정하는 경우 데이터가 인코딩되기 바로 전에 해당 색상 공간으로 변환되어 클라이언트로 반환됩니다. 색상 관리를 사용하지 않는 경우 회색 음영 또는 CMYK로 변환해야 하는 경우 자동 변환이 사용됩니다.

## 포함된 색상 프로필 {#section-5ff733832d38429fbe02b3c1e9bb94a9}

요청에 대해 `iccEmbed=`을 지정하여 렌더링된 이미지와 연관된 색상 프로파일을 응답 이미지에 포함할 수 있습니다.

`icc=`을 지정하지 않으면 작업 색상 공간의 ICC 프로파일이 포함됩니다. 색상 관리를 사용하지 않도록 설정하고 `icc=`에 지정된 프로필이 없는 경우 프로필이 포함되지 않습니다.

## ICC 프로필 {#section-afeb76068b5042adb83261638e450140}

서버에서 사용하는 모든 색상 프로파일은 ICC 사양을 준수해야 합니다. ICC 프로필 파일은 일반적으로 [!DNL .icc] 또는 [!DNL .icm] 파일 접미사를 가지며 자료 데이터 파일과 함께 있습니다.

출력 프로파일은 `icc=` 명령에서 파일 경로/이름으로 지정할 수 있지만 기본 카탈로그의 ICC 프로파일 맵이나 특정 자료 카탈로그의 모든 프로파일 파일을 등록하고 파일 경로 대신 바로 가기 식별자( `icc::Name`)를 사용하는 것이 좋습니다.

작업 프로파일을 재료 카탈로그 또는 기본 카탈로그의 ICC 프로파일 맵에 등록해야 합니다.
