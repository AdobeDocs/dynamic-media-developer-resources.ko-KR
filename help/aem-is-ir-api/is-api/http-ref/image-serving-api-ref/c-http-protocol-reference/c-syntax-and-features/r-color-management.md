---
description: 이미지 제공은 ICC(International Color Consortium) 사양을 준수하는 색상 공간 프로파일을 기반으로 색상 공간 변환을 지원합니다.
seo-description: 이미지 제공은 ICC(International Color Consortium) 사양을 준수하는 색상 공간 프로파일을 기반으로 색상 공간 변환을 지원합니다.
seo-title: 이미지 제공 색상 관리
solution: Experience Manager
title: 이미지 제공 색상 관리
topic: Scene7 Image Serving - Image Rendering API
uuid: 6291372e-ec4c-4fbd-bffc-b55b1bf2f8cf
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# 이미지 제공 색상 관리{#image-serving-color-management}

이미지 제공은 ICC(International Color Consortium) 사양을 준수하는 색상 공간 프로파일을 기반으로 색상 공간 변환을 지원합니다.

## 기본 색상 공간 {#section-8cfe60808bce49968091995e4e521dba}

각 이미지 카탈로그(및 기본 카탈로그)는 이 카탈로그의 기본 색상 공간을 구성하는 ICC 프로파일 세트를 정의할 수 있습니다. 이 프로파일 세트는 회색 음영, RGB 및 CMYK 데이터에 대해 각각 하나의 입력 및 하나의 출력 프로파일을 생성합니다. See ` [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df)`, ` [attribute::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35)`, ` [attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)`, ` [attribute::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2)`, ` [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)`, and ` [attribute::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728)`.

## 입력 색상 공간 {#section-9f08e2c1b6aa4fe4815be174972c1944}

소스 이미지는 ICC 프로파일을 포함하여 입력 색상 공간을 정의할 수 있습니다. 소스 이미지에 프로파일이 포함되지 않은 경우 소스 이미지의 픽셀 유형에 해당하는 `attribute::IccProfileSrc*` 해당 이미지 카탈로그가 사용됩니다. 이미지 카탈로그에 이 속성이 정의되지 않은 경우 이 속성이 `attribute::IccProfile*` 사용됩니다. 해당 카탈로그 속성이 정의되지 않은 경우 이미지는 색상 관리가 되지 않으며 단순 변환만 적용됩니다.

## 출력 색상 공간 {#section-b517bca622b64dcfa7defba6035d0716}

요청의 최종 이미지 결과의 색상 공간은 `icc=` 명령으로 정의됩니다. 지정하지 `icc=` 않으면 출력 이미지의 픽셀 유형에 해당하는 기본 출력 색상 공간(요청의 기본 카탈로그에서)이 출력 색상 공간으로 사용됩니다. 기본 또는 기본 카탈로그에 출력 프로파일이 정의되지 않은 경우 기본 레이어가 출력 픽셀 유형과 일치하는 포함된 프로파일이 있는 이미지인 경우 해당 프로파일이 출력 색상 공간에 사용됩니다. 그렇지 않으면 출력 색상 공간은 정의되지 않은 상태로 유지됩니다. 픽셀 유형 간에 변환할 때 단순 색상 변환만 적용되고 출력 이미지에 색상 프로파일을 포함할 수 없습니다.

중첩된 이미지 제공 요청의 출력 색상 공간은 항상 외부 포함 요청의 출력 색상 공간과 동일합니다.

## 단색 {#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

색상 값에 접미사 &#39;S&#39;가 포함되어 있는 경우, `color=``bgcolor=`또는 RTF 명령으로 지정된 색상 값이 입력 색상 공간과 `\iscolortbl` 연결되어 있고, 그렇지 않으면 출력 색상 공간과 연결됩니다. 또는 RTF 명령으로 `bgc=` 지정된 색상 값을 `\colortbl` 항상 해당 기본 또는 실제 출력 색상 공간과 `\cmykcolortbl` 연결합니다.

>[!NOTE]
>
>현재, 색상 관리에 완전히 참여하지 `bgc=` 않습니다. &#39;S&#39; 접미사는 로 지정하면 무시됩니다. `bgc=`그리고 지정된 색상 값의 픽셀 유형이 출력 이미지의 픽셀 유형과 `bgc=` 다를 때 단순 변환이 적용됩니다. 그렇지 않으면, 는 실제 출력 색상 공간과 `bgc=` 연결됩니다.

## 중첩된 요청 및 포함된 요청 {#section-bdda638c31504f26a77e51ebb1ea6e3b}

중첩된 요청이 에 명시적 출력 색상 공간을 지정하지 않는 한 중첩된 IS 요청과 임베디드 IR 요청에 대한 출력 색상 공간은 가장 바깥쪽 요청의 출력 색상 공간으로 자동으로 설정됩니다 `icc=`. 또한 중첩/임베디드 요청은 가장 바깥쪽 요청의 기본 카탈로그에서 기본 출력 색상 공간을 상속하므로 단색 값을 일관되게 처리합니다.

## 색상 공간 변환 {#section-ca87b80b8e364ea59d8a92d87121b0fb}

이미지 제공은 일반적으로 처리 중에 색상 변환을 지연시킵니다. 이미지의 모든 레이어에 동일한 레이어 색상 공간이 있는 경우 병합 및 최종 크기 조정 후 출력 색상 공간으로 변환됩니다. 여러 개의 레이어 색상 공간이 포함된 경우 병합하기 전에 각 레이어가 출력 색상 공간으로 변형됩니다.

>[!NOTE]
>
>명령, `op_brightness=``op_colorbalance=`, `op_colorize=``op_contrast=`, `op_hue=`및 RGB `op_saturation=` 작업입니다. 이러한 작업은 레이어 색상 공간에 RGB 픽셀 유형이 있는 경우에만 색상 품질을 유지합니다. RGB가 아닌 경우, 데이터는 RGB로 변환되어 색상 충실도가 제한됩니다. 이러한 레이어의 레이어 색상 공간은 결정되지 않은 것으로 간주해야 합니다.

색상 변환 옵션은 `icc=` 또는, 지정되지 않은 경우, 와 함께 `icc=` 또는 와 함께 `attribute::IccRenderIntent`제공됩니다 `attribute::IccBlackPointCompensation``attribute::IccDither`.

## 색상 프로파일 포함 {#section-261ebbae5ce046589a776ca972380052}

출력 색상 공간의 ICC 색상 프로파일(사용 가능한 경우)을 지정하여 응답 이미지에 임베드할 수 `iccEmbed=`있습니다.

## ICC 프로파일 관리 {#section-eb210e4b44e64e2c8b80ee59216c5555}

서버에서 사용하는 모든 색상 프로필은 ICC 사양을 준수해야 합니다. ICC 프로필 파일은 일반적으로 [!DNL .icc] 또는 [!DNL .icm] 파일 접미어를 사용하며 이미지 데이터 파일과 함께 위치합니다.

출력 프로필은 `icc=` 명령에서 파일 경로/이름으로 지정할 수 있지만 기본 카탈로그 또는 이미지 카탈로그의 ICC 프로필 맵에서 모든 프로필 파일을 등록하고 파일 경로 대신 바로 가기 식별자( `icc::Name`)를 사용하는 것이 좋습니다.

에서 참조되거나 에서 참조되는 모든 ICC 프로필은 `catalog::IccProfile` 이미지 또는 기본 카탈로그의 ICC 프로필 맵에 등록되어 `attribute::IccProfile*` 있어야 합니다.

## Restrictions {#section-fb50ede40b124b89b30679da29782ab5}

현재 CMYK, RGB 및 회색 음영 색상 공간만 지원됩니다.

## 포함된 ICC 색상 프로파일 {#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

이미지 제공 기본 이미지 카탈로그에는 대부분의 표준 Adobe ICC 프로필이 포함되어 있습니다. 이러한 프로필은 공통 이름(예: Photoshop에서 표시)이나 보다 짧은 식별자로 액세스할 수 있습니다. 다음 표에는 모든 표준 ICC 프로파일이 나열되어 있습니다. 공통 이름으로 `icc=` 명령의 프로파일을 참조할 때는 공백을 로 인코딩해야 합니다 `%20`.

기본 카탈로그 또는 특정 이미지 카탈로그에 표준 프로필에 추가 프로필을 추가할 수 있습니다. 자세한 내용은 [ICC 프로필](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) 맵 참조를 참조하십시오.

>[!NOTE]
>
>다음 표는 Dynamic Media *Hybrid에만* 적용됩니다( `dynamicmedia` 실행 모드에서 실행).

|ID|일반 이름|파일 이름||—|—|—||**RGB**||||`AdobeRGB`|Adobe RGB(1998)|AdobeRGB1998.icc||`AppleRGB`|Apple RGB|AppleRGB.icc||`CIERGB`|CIE RGB|CIERGB.icc||`ColorMatchRGB`|ColorMatch RGB|ColorMatchRGB.icc||`NTSC`|NTSC(1953)|NTSC1953.icc||`PAL`|PAL/SECAM|PAL_SECAM.icc||`ProPhoto`|ProPhoto RGB|ProPhoto.icm||`SMPTE`|SMPTE-C|SMPTE-C.icc||`sRGB`|sRGB IEC61966-2.1|sRgb 색상 공간 프로필.icm||`WideGamutRGB`|넓은 색상 영역 RGB|WideColorRGB.icc||**CMYK**||||`CoatedFogra27`|Coated FOGRA27(ISO 12647-2:2004)|CoatedFOGRA27.icc||`CoatedFogra39`|Coated FOGRA39(ISO 12647-2:2004)|CoatedFOGRA39.icc||`CoatedGraCol`|Coated GRACoL 2006(ISO 12647-2:2004)|CoatedGRACoL2006.icc||`EuropeISOCoated`|Europe ISO Coated FOGRA27|EuropeISOCoatedFOGRA27.icc||`EuroscaleCoated`|Euroscale Coated|EuroscaleCoated.icc||`EuroscaleUncoated`|Euroscale Uncoated v2|EuroscaleUncoated.icc||`JapanColorCoated`|Japan Color 2001 Coated|JapanColor2001Coated.icc||`JapanColorNewspaper`|Japan Color 2002 Newspaper|JapanColor2002Newspaper.icc||`JapanColorUncoated`|Japan Color 2001 Uncoated|JapanColor2001Uncoated.icc||`JapanColorWebCoated`|Japan Color 2003 Web Coated|JapanColor2003WebCoated.icc||`JapanWebCoated`|Japan Web Coated(광고)|JapanWebCoated.icc||`NewsprintSNAP2007`|US Newsprint(SNAP 2007)|USNewsprintSNAP2007.icc||`PS4Default`|Photoshop 4 기본 CMYK|Photoshop4DefaultCMYK.icc||`PS5Default`|Photoshop 5 기본 CMYK|Photoshop5DefaultCMYK.icc||`SheetfedCoated`|미국Sheetfed Coated v2|USSheetfedCoated.icc||`SheetfedUncoated`|미국Sheetfed Uncoated v2|USSheetfedUncoated.icc||`UncoatedFogra29`|Uncoated FOGRA29 (ISO 12647-2:2004)|UncoatedFOGRA29.icc||`WebCoated`|미국Web Coated(SWOP) v2|USWebCoatedSWOP.icc||`WebCoatedFogra28`|Web Coated FOGRA28 (ISO 12647-2:2004)|WebCoatedFOGRA28.icc||`WebCoatedGrade3`|Web Coated SWOP 2006 Grade 3 Paper|WebCoatedSWOP2006Grade3.icc||`WebCoatedGrade5`|Web Coated SWOP 2006 Grade 5 Paper|WebCoatedSWOP2006Grade5.icc||`WebUncoated`|미국Web Uncoated v2|USWebUncoated.icc|

다음 표는 Dynamic Media *Classic(Scene7) 이미지 제공* 및 *다이내믹 미디어* ( `dynamicmedia_scene7` 실행 모드에서 실행)에적용됩니다.

|ID|일반 이름|파일 이름||—|—|—||**RGB**||||`AdobeRGB`|Adobe RGB(1998)|AdobeRGB1998.icc||`AppleRGB`|Apple RGB|AppleRGB.icc||`CIERGB|CIE RGB`|CIERGB.icc||`ColorMatchRGB`|ColorMatch RGB|ColorMatchRGB.icc||`NTSC`|NTSC(1953)|NTSC1953.icc||`PAL`|PAL/SECAM|PAL_SECAM.icc||`ProPhoto RGB`|ProPhoto RGB|ProPhoto RGB.icm||`SMPTE`|SMPTE-C|SMPTE-C.icc||`sRGB`|sRGB IEC61966-2.1|sRgb 색상 공간 프로필.icm||`WideGamutRGB`|넓은 색상 영역 RGB|WideColorRGB.icc||**CMYK**||||`CoatedFogra27`|Coated FOGRA27(ISO 12647-2:2004)|CoatedFOGRA27.icc||`CoatedFogra39`|Coated FOGRA39(ISO 12647-2:2004)|CoatedFOGRA39.icc||`Coated GRACoL 2006 (ISO 12647-2:2004)`|Coated GRACoL 2006(ISO 12647-2:2004)|CoatedGRACoL2006.icc||`EuropeISOCoated`|Europe ISO Coated FOGRA27|EuropeISOCoatedFOGRA27.icc||`Euroscale Coated v2`|Euroscale Coated v2|EuroscaleCoated.icc||`EuroscaleUncoated`|Euroscale Uncoated v2|EuroscaleUncoated.icc||`JapanColorCoated`|Japan Color 2001 Coated|JapanColor2001Coated.icc||`JapanColorNewspaper`|Japan Color 2002 Newspaper|JapanColor2002Newspaper.icc||`JapanColorUncoated`|Japan Color 2001 Uncoated|JapanColor2001Uncoated.icc||`Japan Color 2003 Web Coated`|Japan Color 2003 Web Coated|JapanColor2003WebCoated.icc||`JapanWebCoated`|Japan Web Coated(광고)|JapanWebCoated.icc||`PS4Default`|Photoshop 4 기본 CMYK|Photoshop4DefaultCMYK.icc||`PS5Default`|Photoshop 5 기본 CMYK|Photoshop5DefaultCMYK.icc||`SheetfedCoated`|미국Sheetfed Coated v2|USSheetfedCoated.icc||`SheetfedUncoated`|미국Sheetfed Uncoated v2|USSheetfedUncoated.icc||`UncoatedFogra29`|Uncoated FOGRA29 (ISO 12647-2:2004)|UncoatedFOGRA29.icc||`US Newsprint (SNAP 2007)`|US Newsprint(SNAP 2007)|USNewsprintSNAP2007.icc||`WebCoated`|미국Web Coated(SWOP) v2|USWebCoatedSWOP.icc||`WebCoatedFogra28`|Web Coated FOGRA28 (ISO 12647-2:2004)|WebCoatedFOGRA28.icc||`Web Coated SWOP 2006 Grade 3 Paper`|Web Coated SWOP 2006 Grade 3 Paper|WebCoatedSWOP2006Grade3.icc||`Web Coated SWOP Grade 5 Paper`|Web Coated SWOP 2006 Grade 5 Paper|WebCoatedSWOP2006Grade5.icc||`WebUncoated`|미국Web Uncoated v2|USWebUncoated.icc|

## 참조 {#section-39159397e80b4efca5f631eab8b9aa06}

[국제 색상](http://www.color.org/index.xalter), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [속성::icc프로필](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)*, 속성: icc프로필:icc [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)[](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)[ src, src* 컨소시엄:icc:icc 속성:iccrenderIntentInIn속성:검정:IccCombedPointCompensationDiicc: 다른 방법으로는, ICC 프로파일 맵 참조, 색상=에 대한 언급이 있습니다. *`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
