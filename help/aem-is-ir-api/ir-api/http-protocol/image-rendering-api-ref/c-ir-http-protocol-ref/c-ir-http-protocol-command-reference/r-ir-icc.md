---
description: 출력 색상 프로파일.
seo-description: 출력 색상 프로파일.
seo-title: icc
solution: Experience Manager
title: icc
topic: Scene7 Image Serving - Image Rendering API
uuid: 95a05fe5-d6b3-4118-aab4-4664ccee2850
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 1%

---


# icc{#icc}

출력 색상 프로파일.

icc= *`profile`*[, *`renderIntent`*[,*`blackpointComp`*]]

<table id="simpletable_DF1914FD351E4F2BA61372A52F0CFFBF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 프로필</span></span> </p></td> 
  <td class="stentry"> <p>ICC 색상 프로파일. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent  </span> </span> </p></td> 
  <td class="stentry"> <p>지각 | 상대 | 채도 | 절대 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span> </span> </p></td> 
  <td class="stentry"> <p>1을 사용하여 블랙포인트 보정을 비활성화하려면 0을 사용합니다. </p></td> 
 </tr> 
</table>

*`profile`* 렌더링된 이미지가 작업 프로필과 다른 경우 변환할 출력 색상 공간 프로파일을 지정합니다. *`profile`* 는 이미지 카탈로그의 ICC 프로필 맵이나 기본 카탈로그의 유효한  `icc::Name` ICC 프로필 맵에 정의되어 있거나 프로필 파일의 상대 경로(일반적으로  [!DNL .icc]또는  [!DNL .icm] 접미어 포함)여야 합니다.

>[!NOTE]
>
>*`profile`* HTTP로 인코딩된 경우에도 &#39;,&#39; 문자를 포함할 수 없습니다.

*`renderIntent`* 기본 렌더링 의도를 재정의할 수 있습니다.

*`blackpointComp`* 출력 프로파일이 이 기능을 지원하는 경우 blackpoint 보상을 활성화합니다.

>[!NOTE]
>
>일부 색상 변환은 모든 *`renderIntent`* 및 *`blackpointComp`* 선택 항목을 지원하지 않습니다. 일반적으로 이러한 설정은 ICC 출력 프로파일이 프린터 또는 모니터와 같은 출력 장치를 지정하는 경우에만 적용됩니다. 또한 일부 ICC 출력 프로필은 일부 *`renderIntent`* 선택 항목을 지원하지 않습니다.

## 속성 {#section-b4042623a8ea40248c11b2153e5906b1}

요청 내 어느 곳에서든 발생할 수 있습니다. `fmt=`으로 지정된 이미지 유형이 *`profile`*&#x200B;과(와) 일치하지 않으면 오류가 반환됩니다.

*`renderIntent`* 및 *`blackpointComp`* 는 지정된 ICC 프로파일과 호환하지 않으면 무시됩니다.

CMYK 출력 장치 프로파일은 서로 다른 렌더링 의도를 지원할 가능성이 높습니다.

## 기본값 {#section-bbd3206fdcac4dc48a08fc9eba14fc90}

색상 관리가 활성화되어 있고 `icc=`이 지정되지 않은 경우 서버는 `fmt=`로 지정된 이미지 유형과 일치하는 출력 프로필( `attribute::IccProfile*`)으로 변환된 이미지를 전달합니다.

지정하지 않으면 *`renderIntent`*&#x200B;은 `attribute::IccRenderIntent`에서 상속되고 *`blackpointComp`*&#x200B;는 `attribute::IccBlackPointCompensation`에서 상속됩니다.

## 참조 {#section-37ef83149fd74345956a98f633cc0294}

[색상 관리](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-color-management.md#concept-7bac7c2c41be42c1b301eae80abe6b8d),  [속성::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127),  [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f),  [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)  [ ](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)  [, 속성:IccRenderIntent, 속성::iccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0)
