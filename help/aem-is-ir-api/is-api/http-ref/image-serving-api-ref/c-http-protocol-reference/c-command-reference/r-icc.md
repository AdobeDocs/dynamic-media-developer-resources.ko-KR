---
description: 출력 색상 프로필.
seo-description: 출력 색상 프로필.
seo-title: icc
solution: Experience Manager
title: icc
topic: Scene7 Image Serving - Image Rendering API
uuid: cfbd18aa-cbba-4085-920d-1f54645d0f89
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# icc{#icc}

출력 색상 프로필.

`icc= *``*[, *``*[, *``*[, *`objectrenderIntentblackpointComdither`*]]`

<table id="simpletable_AC20916999004CDCBBB9888B3A8FB0A7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 개체</span></span> </p></td> 
  <td class="stentry"> <p>ICC 색상 프로파일 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 렌더링 <span class="varname"> 의도</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> perception|relative|saturation|absolute</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span></span> </p></td> 
  <td class="stentry"> <p>1을 활성화하려면 0을 클릭하여 블랙포인트 보상을 비활성화합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 디더</span></span> </p></td> 
  <td class="stentry"> <p>1 - 활성화, 디더링 비활성화 </p></td> 
 </tr> 
</table>

*`object`* 작업 프로필과 다른 경우 이미지를 변환할 출력 색상 공간 프로파일을 지정합니다. *`profile`* 는 이미지 카탈로그의 ICC 프로필 맵이나 기본 카탈로그의 올바른 `icc::Name` 정의되거나 프로필 파일의 상대 경로(일반적으로 [!DNL .icc] 또는 [!DNL .icm] 접미사를 가진 경로)여야 합니다. 자세한 내용은 [ 을 *`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)참조하십시오.

>[!NOTE]
>
>*`object`* HTTP로 인코딩된 경우에도 &#39;,&#39; 문자를 포함할 수 없습니다.

*`renderIntent`* 에서 기본 렌더링 의도를 재정의할 수 있습니다.

*`blackpointComp`* 출력 프로파일이 이 기능을 지원하는 경우 블랙포인트 보정을 활성화합니다.

>[!NOTE]
>
>일부 색상 변환은 모든 *`renderIntent`* 색상 및 *`blackpointComp`* 선택 사항을 지원하지 않습니다. 일반적으로 이러한 설정은 ICC 출력 프로파일이 프린터 또는 모니터와 같은 출력 장치를 특징으로 하는 경우에만 적용됩니다. 또한 일부 ICC 출력 프로필은 일부 *`renderIntent`* 옵션을 지원하지 않습니다.

참고

*`dither`* 색상 밴딩 결함을 방지하거나 줄일 수 있는 디더링(실제로 오류 확산)을 활성화합니다.

## 속성 {#section-9fcd3e7bd1fd43c887b0f18a2f3c7259}

요청 속성입니다. 일치하지 않는 이미지 형식을 지정한 경우 서버에서 오류를 반환합니다. `fmt=` 이 *`profile`*&#x200B;경우

*`renderIntent`* 지정된 ICC 프로파일과 호환하지 않으면 *`blackpointComp`* 무시됩니다. CMYK 출력 장치 프로파일은 서로 다른 렌더링 의도를 지원할 가능성이 높습니다.

## 기본값 {#section-0b9fe2eb428447df8ae9948f11ab5aae}

색상 관리가 활성화되어 있고 `icc=` 지정되지 않은 경우 서버는 에서 지정한 이미지 유형과 일치하는 출력 프로필( `attribute::IccProfile*`)으로 변환된 이미지를 제공합니다 `fmt=`.

지정하지 않으면 *`renderIntent`* 에서 상속되고 에서 상속되며 `attribute::IccRenderIntent`에서 상속되며 *`blackpointComp`* 상속됩니다 `attribute::IccBlackPointCompensation`*`dither`* `attribute::IccDither`.

## 참조 {#section-37f16b0c2c4b48f3a39dcde2a350f91e}

[속성::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) , [속성::RenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [:IccPoint](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [속성:IccPoint](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b), fmt=, FMT, 객체 [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)[관리, 색상 관리, ICC 프로파일 참조, ICC프로필 참조, iccIccAttribute embed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)
