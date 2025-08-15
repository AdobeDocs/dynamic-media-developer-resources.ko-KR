---
title: 이미지 제공 색상 관리
description: 이미지 제공은 ICC(International Color Consortium) 사양을 따르는 색상 공간 프로파일을 기반으로 색상 공간 변환을 지원합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c9a489c-36e0-4934-b9c5-33414a9ce0b8
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1210'
ht-degree: 0%

---

# 이미지 제공 색상 관리{#image-serving-color-management}

이미지 제공은 ICC(International Color Consortium) 사양을 따르는 색상 공간 프로파일을 기반으로 색상 공간 변환을 지원합니다.

## 기본 색상 공간 {#section-8cfe60808bce49968091995e4e521dba}

각 이미지 카탈로그(및 기본 카탈로그)는 이 카탈로그의 기본 색상 공간을 구성하는 ICC 프로파일 세트(각각 회색 음영, RGB 및 CMYK 데이터에 대한 입력 및 출력 프로파일 하나)를 정의할 수 있습니다. 다음을 참조하십시오
[attribute::IccProfileRgb](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md)
[attribute::IccProfileGray](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md)
[attribute::IccProfileCmyk](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md)
[attribute::IccProfileSrcRgb](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md)
[attribute::IccProfileSrcGray](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md)
[attribute::IccProfileSrcCmyk](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md).

## 입력 색상 공간 {#section-9f08e2c1b6aa4fe4815be174972c1944}

Source 이미지는 ICC 프로파일을 포함하여 입력 색상 공간을 정의할 수 있습니다. 소스 이미지에 포함된 프로필이 없으면 소스 이미지의 픽셀 유형에 해당하는 적용 가능한 이미지 카탈로그의 `attribute::IccProfileSrc*`이(가) 사용됩니다. 이 특성이 이미지 카탈로그에 정의되어 있지 않으면 `attribute::IccProfile*`이(가) 사용됩니다. 해당 카탈로그 속성이 정의되지 않은 경우 이미지는 색상 관리되지 않으며 순진한 변환만 적용됩니다.

## 출력 색상 공간 {#section-b517bca622b64dcfa7defba6035d0716}

`icc=` 명령을 사용하여 요청의 최종 이미지 결과의 색 공간을 정의합니다. `icc=`을(를) 지정하지 않으면 출력 이미지의 픽셀 유형에 해당하는 기본 출력 색상 공간(요청의 주 카탈로그에서)이 출력 색상 공간으로 사용됩니다. 기본 카탈로그나 기본 카탈로그에 출력 프로파일이 정의되어 있지 않고 기본 레이어가 출력 픽셀 유형과 일치하는 프로파일이 포함된 이미지인 경우 해당 프로파일이 출력 색상 공간에 사용됩니다. 그렇지 않으면 출력 색상 공간이 정의되지 않은 상태로 유지됩니다. 즉, 픽셀 유형 간에 변환할 때는 순한 색상 변환만 적용되고 출력 이미지에 색상 프로파일을 포함할 수 없습니다.

중첩/임베드된 이미지 제공 요청의 출력 색상 공간은 항상 외부 임베드 요청의 출력 색상 공간과 동일합니다.

## 단색 {#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

`color=`, `bgcolor=` 또는 RTF 명령 `\iscolortbl`(으)로 지정된 색상 값은 색상 값에 접미사 &#39;S&#39;가 포함되어 있으면 입력 색상 공간과 연결되고, 그렇지 않으면 출력 색상 공간과 연결됩니다. `bgc=` 또는 RTF 명령 `\colortbl` 및 `\cmykcolortbl`에 지정된 색상 값은 항상 해당 기본 또는 실제 출력 색상 공간과 연결됩니다.

>[!NOTE]
>
>현재 `bgc=`은(는) 색상 관리에 완전히 참여하지 않습니다. `bgc=`(으)로 지정된 경우 &#39;S&#39; 접미사는 무시되며, `bgc=`(으)로 지정된 색상 값의 픽셀 유형이 출력 이미지의 픽셀 유형과 다른 경우 순조로운 변환이 적용됩니다. 그렇지 않으면 `bgc=`이(가) 실제 출력 색상 공간과 연결됩니다.

## 중첩 및 포함된 요청 {#section-bdda638c31504f26a77e51ebb1ea6e3b}

중첩된 요청이 `icc=`을(를) 사용하여 명시적 출력 색상 공간을 지정하지 않는 한 중첩된 IS 요청 및 포함된 IR 요청에 대한 출력 색상 공간은 가장 바깥쪽 요청의 출력 색상 공간으로 자동 설정됩니다. 또한 중첩된/포함된 요청은 가장 바깥쪽 요청의 기본 카탈로그에서 기본 출력 색상 공간을 상속하여 단색 값을 일관되게 처리합니다.

## 색상 공간 변환 {#section-ca87b80b8e364ea59d8a92d87121b0fb}

이미지 제공은 일반적으로 처리 중에 색상 변환을 지연하려고 합니다. 이미지의 모든 레이어에 동일한 레이어 색상 공간이 있는 경우 병합 및 최종 크기 조정 후에 출력 색상 공간으로 변환됩니다. 여러 레이어 색상 공간이 포함된 경우 병합하기 전에 각 레이어가 출력 색상 공간으로 변형됩니다.

>[!NOTE]
>
>`op_brightness=`, `op_colorbalance=`, `op_colorize=`, `op_contrast=`, `op_hue=` 및 `op_saturation=` 명령은 RGB 작업입니다. 이러한 작업은 레이어 색상 공간에 RGB 픽셀 유형이 있는 경우에만 색상 충실도를 유지합니다. RGB 이외의 경우 순한 색상 변환을 사용하여 데이터가 RGB으로 변환되며 그 결과 색상 충실도가 제한됩니다. 이러한 레이어들에 대한 레이어 색상 공간은 결정되지 않은 것으로 간주되어야 한다.

색상 변환 옵션은 `icc=`과(와) 함께 제공되거나, `icc=`이(가) 지정되지 않은 경우 `attribute::IccRenderIntent`, `attribute::IccBlackPointCompensation` 및 `attribute::IccDither`과(와) 함께 제공됩니다.

## 색상 프로파일 포함 {#section-261ebbae5ce046589a776ca972380052}

사용 가능한 경우 `iccEmbed=`을(를) 지정하여 출력 색상 공간의 ICC 색상 프로파일을 응답 이미지에 포함할 수 있습니다.

## ICC 프로파일 관리 {#section-eb210e4b44e64e2c8b80ee59216c5555}

서버에서 사용하는 모든 색상 프로파일은 ICC 사양을 준수해야 합니다. ICC 프로필 파일에는 일반적으로 [!DNL .icc] 또는 [!DNL .icm] 파일 접미사가 있으며 이미지 데이터 파일과 함께 위치합니다.

`icc=` 명령에서 파일 경로/이름으로 출력 프로필을 지정할 수 있지만 기본 카탈로그 또는 이미지 카탈로그의 ICC 프로필 맵에 모든 프로필 파일을 등록하고 파일 경로 대신 바로 가기 식별자(`icc::Name`)를 사용하는 것이 좋습니다.

`catalog::IccProfile` 및 `attribute::IccProfile*`에서 참조된 모든 ICC 프로필은 이미지 또는 기본 카탈로그의 ICC 프로필 맵에 등록해야 합니다.

## 제한 사항 {#section-fb50ede40b124b89b30679da29782ab5}

현재는 CMYK, RGB 및 회색 음영 색상 공간만 지원됩니다.

## 포함된 ICC 색상 프로파일 {#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

이미지 제공에는 기본 이미지 카탈로그에 있는 대부분의 표준 Adobe ICC 프로필이 포함됩니다. 이러한 프로필은 일반적인 이름(예: Photoshop에 표시됨)이나 더 짧은 식별자를 사용하여 액세스할 수 있습니다. 다음 표에는 모든 표준 ICC 프로파일이 나열되어 있습니다. `icc=` 명령의 프로필을 공통 이름으로 참조할 때 공백은 `%20`(으)로 인코딩해야 합니다.

기본 카탈로그나 특정 이미지 카탈로그에 추가 프로필을 표준 프로필에 추가할 수 있습니다. 자세한 내용은 [ICC 프로필 맵 참조](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)를 참조하십시오.

>[!NOTE]
>
>다음 표는 *Dynamic Media 하이브리드*&#x200B;에만 적용됩니다(`dynamicmedia` 실행 모드에서 실행).

| 식별자 | 일반 이름 | 파일 이름 |
|-- |-- |-- |
| **RGB** |  |  |
| `AdobeRGB` | Adobe RGB (1998) | AdobeRGB1998.icc |
| `AppleRGB` | Apple RGB | AppleRGB.icc |
| `CIERGB` | CIE RGB | CIERGB.icc |
| `ColorMatchRGB` | ColorMatch RGB | ColorMatchRGB.icc |
| `NTSC` | NTSC(1953) | NTSC1953.icc |
| `PAL` | PAL/SECAM | PAL_SECAM.icc |
| `ProPhoto` | ProPhoto RGB | ProPhoto.icm |
| `SMPTE` | SMPTE-C | SMPTE-C.icc |
| `sRGB` | sRGB IEC61966-2.1 | sRgb 색상 공간 Profile.icm |
| `WideGamutRGB` | 광영역 RGB | WideGamutRGB.icc |
| **CMYK** |  |  |
| `CoatedFogra27` | 코팅된 FOGRA27(ISO 12647-2:2004) | CoatedFOGRA27.icc |
| `CoatedFogra39` | 코팅된 FOGRA39(ISO 12647-2:2004) | CoatedFOGRA39.icc |
| `CoatedGraCol` | 코팅된 GRACoL 2006(ISO 12647-2:2004) | CoatedGRACoL2006.icc |
| `EuropeISOCoated` | 유럽 ISO 코팅 FOGRA27 | EuropeISOCoatedFOGRA27.icc |
| `EuroscaleCoated` | 유로스케일 코팅 | EuroscaleCoated.icc |
| `EuroscaleUncoated` | Euroscale Uncoated v2 | EuroscaleUncoated.icc |
| `JapanColorCoated` | Japan Color 2001 코팅 | JapanColor2001Coated.icc |
| `JapanColorNewspaper` | 일본 색상 2002 신문 | JapanColor2002Newspaper.icc |
| `JapanColorUncoated` | Japan Color 2001 무코팅 | JapanColor2001Uncoated.icc |
| `JapanColorWebCoated` | Japan Color 2003 웹 코팅 | JapanColor2003WebCoated.icc |
| `JapanWebCoated` | Japan Web Coated (Ad) | JapanWebCoated.icc |
| `NewsprintSNAP2007` | 미국 신문용지(SNAP 2007) | USNewsprintSNAP2007.icc |
| `PS4Default` | Photoshop 4 기본 CMYK | Photoshop4DefaultCMYK.icc |
| `PS5Default` | Photoshop 5 기본 CMYK | Photoshop5DefaultCMYK.icc |
| `SheetfedCoated` | U.S. Sheetfed Coated v2 | USSheetfedCoated.icc |
| `SheetfedUncoated` | 미국 Sheetfed Uncoated v2 | USSheetfedUncoated.icc |
| `UncoatedFogra29` | 코팅되지 않은 FOGRA29(ISO 12647-2:2004) | UncoatedFOGRA29.icc |
| `WebCoated` | U.S. Web Coated (SWOP) v2 | USWebCoatedSWOP.icc |
| `WebCoatedFogra28` | 웹으로 코팅된 FOGRA28(ISO 12647-2:2004) | WebCoatedFOGRA28.icc |
| `WebCoatedGrade3` | Web Coated SWOP 2006 Grade 3 용지 | WebCoatedSWOP2006Grade3.icc |
| `WebCoatedGrade5` | 웹코팅 SWOP 2006 Grade 5 용지 | WebCoatedSWOP2006Grade5.icc |
| `WebUncoated` | U.S. Web Uncoated v2 | USWebUncoated.icc |

다음 표는 *Dynamic Media Classic 이미지 제공* 및 *Dynamic Media*(`dynamicmedia_scene7` 실행 모드에서 실행)에 적용됩니다.

| 식별자 | 일반 이름 | 파일 이름 |
|-- |-- |-- |
| **RGB** |  |  |
| `AdobeRGB` | Adobe RGB (1998) | AdobeRGB1998.icc |
| `AppleRGB` | Apple RGB | AppleRGB.icc |
| `CIERGB|CIE RGB` | CIERGB.icc |
| `ColorMatchRGB` | ColorMatch RGB | ColorMatchRGB.icc |
| `NTSC` | NTSC(1953) | NTSC1953.icc |
| `PAL` | PAL/SECAM | PAL_SECAM.icc |
| `ProPhoto RGB` | ProPhoto RGB | ProPhoto RGB.icm |
| `SMPTE` | SMPTE-C | SMPTE-C.icc |
| `sRGB` | sRGB IEC61966-2.1 | sRgb 색상 공간 Profile.icm |
| `WideGamutRGB` | 광영역 RGB | WideGamutRGB.icc |
| **CMYK** |  |  |
| `CoatedFogra27` | 코팅된 FOGRA27(ISO 12647-2:2004) | CoatedFOGRA27.icc |
| `CoatedFogra39` | 코팅된 FOGRA39(ISO 12647-2:2004) | CoatedFOGRA39.icc |
| `Coated GRACoL 2006 (ISO 12647-2:2004)` | 코팅된 GRACoL 2006(ISO 12647-2:2004) | CoatedGRACoL2006.icc |
| `EuropeISOCoated` | 유럽 ISO 코팅 FOGRA27 | EuropeISOCoatedFOGRA27.icc |
| `Euroscale Coated v2` | Euroscale Coated v2 | EuroscaleCoated.icc |
| `EuroscaleUncoated` | Euroscale Uncoated v2 | EuroscaleUncoated.icc |
| `JapanColorCoated` | Japan Color 2001 코팅 | JapanColor2001Coated.icc |
| `JapanColorNewspaper` | 일본 색상 2002 신문 | JapanColor2002Newspaper.icc |
| `JapanColorUncoated` | Japan Color 2001 무코팅 | JapanColor2001Uncoated.icc |
| `Japan Color 2003 Web Coated` | Japan Color 2003 웹 코팅 | JapanColor2003WebCoated.icc |
| `JapanWebCoated` | Japan Web Coated (Ad) | JapanWebCoated.icc |
| `PS4Default` | Photoshop 4 기본 CMYK | Photoshop4DefaultCMYK.icc |
| `PS5Default` | Photoshop 5 기본 CMYK | Photoshop5DefaultCMYK.icc |
| `SheetfedCoated` | U.S. Sheetfed Coated v2 | USSheetfedCoated.icc |
| `SheetfedUncoated` | 미국 Sheetfed Uncoated v2 | USSheetfedUncoated.icc |
| `UncoatedFogra29` | 코팅되지 않은 FOGRA29(ISO 12647-2:2004) | UncoatedFOGRA29.icc |
| `US Newsprint (SNAP 2007)` | 미국 신문용지(SNAP 2007) | USNewsprintSNAP2007.icc |
| `WebCoated` | U.S. Web Coated (SWOP) v2 | USWebCoatedSWOP.icc |
| `WebCoatedFogra28` | 웹으로 코팅된 FOGRA28(ISO 12647-2:2004) | WebCoatedFOGRA28.icc |
| `Web Coated SWOP 2006 Grade 3 Paper` | Web Coated SWOP 2006 Grade 3 용지 | WebCoatedSWOP2006Grade3.icc |
| `Web Coated SWOP Grade 5 Paper` | 웹코팅 SWOP 2006 Grade 5 용지 | WebCoatedSWOP2006Grade5.icc |
| `WebUncoated` | U.S. Web Uncoated v2 | USWebUncoated.icc |

## 참조 {#section-39159397e80b4efca5f631eab8b9aa06}

[International Color Consortium](https://www.color.org/index.xalter), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [attribute::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)&#42;, [attribute::IccProfileSrc](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)&#42;, [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [attribute::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b), [ICC 프로필 맵 참조](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c), [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [*`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
