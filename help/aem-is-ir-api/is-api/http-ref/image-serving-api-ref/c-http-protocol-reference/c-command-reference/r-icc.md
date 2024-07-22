---
title: icc
description: 출력 색상 프로파일.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8be7be8c-a23d-4a5b-93e4-44231155616b
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 1%

---

# icc{#icc}

출력 색상 프로파일.

`icc= *`개체`*[, *`renderIntent`*[, *`blackpointComp`*[, *`디더`*]]`

<table id="simpletable_AC20916999004CDCBBB9888B3A8FB0A7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 개체</span> </span> </p></td> 
  <td class="stentry"> <p>ICC 색상 프로파일. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 가시 범위|상대|채도|절대</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span></span> </p></td> 
  <td class="stentry"> <p>활성화하려면 1을 사용하고, 검은 점 보상을 비활성화하려면 0을 사용합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 디더</span></span> </p></td> 
  <td class="stentry"> <p>활성화하려면 1을 사용하고, 디더링을 비활성화하려면 0을 사용합니다. </p></td> 
 </tr> 
</table>

*`object`* 값은 작업 프로필과 다른 경우 이미지를 변환해야 하는 출력 색상 공간 프로필을 지정합니다. 값 *`profile`*&#x200B;은(는) 이미지 카탈로그 또는 기본 카탈로그의 ICC 프로필 맵에 정의된 올바른 `icc::Name`이거나 프로필 파일에 대한 상대 경로여야 합니다(일반적으로 [!DNL .icc] 또는 [!DNL .icm] 접미사를 사용). 자세한 내용은 [*`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)을(를) 참조하십시오.

>[!NOTE]
>
>값 *`object`*&#x200B;은(는) HTTP로 인코딩된 경우에도 &#39;,&#39; 문자를 포함할 수 없습니다.

값 *`renderIntent`*&#x200B;을(를) 사용하면 기본 렌더링 의도를 재정의할 수 있습니다.

출력 프로필에서 이 기능을 지원하는 경우 값 *`blackpointComp`*&#x200B;을(를) 사용하면 검은 점 보상을 사용할 수 있습니다.

>[!NOTE]
>
>일부 색상 변환에서는 모든 *`renderIntent`* 및 *`blackpointComp`* 선택을 지원하지 않습니다. 일반적으로 이러한 설정은 ICC 출력 프로파일이 프린터 또는 모니터와 같은 출력 장치를 특성화하는 경우에만 적용됩니다. 또한 일부 ICC 출력 프로필은 모든 *`renderIntent`* 선택을 지원하지 않습니다.

참고

수정자 *`dither`*&#x200B;을(를) 사용하면 디더링(실제로 오류 확산)이 가능하므로 색상 밴딩 아티팩트를 방지하거나 줄일 수 있습니다.

## 속성 {#section-9fcd3e7bd1fd43c887b0f18a2f3c7259}

요청 속성입니다. 이미지 형식이 *`profile`*&#x200B;과(와) 일치하지 않는 `fmt=`(으)로 지정된 경우 서버에서 오류를 반환합니다.

지정된 ICC 프로필과 호환되지 않으면 수정자 *`renderIntent`* 및 *`blackpointComp`*&#x200B;이(가) 무시됩니다. CMYK 출력 장치 프로필은 다른 렌더링 의도를 지원할 가능성이 높습니다.

## 기본값 {#section-0b9fe2eb428447df8ae9948f11ab5aae}

색상 관리가 활성화되어 있고 `icc=`이(가) 지정되지 않은 경우 서버는 `fmt=`에 지정된 이미지 유형과 일치하는 출력 프로필(`attribute::IccProfile*`)로 변환된 이미지를 전달합니다.

지정하지 않으면 *`renderIntent`*&#x200B;은(는) `attribute::IccRenderIntent`에서 상속되고, *`blackpointComp`*&#x200B;은(는) `attribute::IccBlackPointCompensation`에서 상속되며, *`dither`*&#x200B;은(는) `attribute::IccDither`에서 상속됩니다.

## 참조 {#section-37f16b0c2c4b48f3a39dcde2a350f91e}

[특성::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) , [특성::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [특성::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [특성::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a), [개체](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0), [색상 관리](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7), [ICC 프로필 맵 참조](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)
