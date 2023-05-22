---
title: icc
description: 출력 색상 프로파일.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39b25f7c-ed3c-4132-8241-e7f3aab07b00
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '232'
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
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent </span> </span> </p></td> 
  <td class="stentry"> <p>인식 | 상대 | 채도 | 절대 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span> </span> </p></td> 
  <td class="stentry"> <p>활성화하려면 1을 사용하고, 검은 점 보상을 비활성화하려면 0을 사용합니다. </p></td> 
 </tr> 
</table>

*`profile`* 렌더링된 이미지가 작업 프로파일과 다른 경우 변환해야 하는 출력 색상 공간 프로파일을 지정합니다. *`profile`* 은(는) 유효한 값이어야 합니다. `icc::Name` 이미지 카탈로그나 기본 카탈로그의 ICC 프로파일 맵 또는 프로파일 파일에 대한 상대 경로에 정의되어 있습니다(일반적으로 [!DNL `.icc`] 또는 [!DNL `.icm`] suffix).

>[!NOTE]
>
>*`profile`* HTTP로 인코딩된 경우에도 &#39;,&#39; 문자를 포함할 수 없습니다.

*`renderIntent`* 기본 렌더링 의도 무시를 허용합니다.

*`blackpointComp`* 출력 프로필에서 이 기능을 지원하는 경우 검은 점 보상을 활성화합니다.

>[!NOTE]
>
>일부 색상 변환만 모두 지원하는 것은 아닙니다. *`renderIntent`* 및 *`blackpointComp`* 선택 사항. 일반적으로 이러한 설정은 ICC 출력 프로파일이 프린터 또는 모니터와 같은 출력 장치를 특성화하는 경우에만 적용됩니다. 또한 일부 ICC 출력 프로파일은 모든 것을 지원하지 않습니다 *`renderIntent`* 선택 사항.

## 속성 {#section-b4042623a8ea40248c11b2153e5906b1}

요청 내의 어느 곳에서든 발생할 수 있습니다. 이미지 유형이 로 지정된 경우 오류가 반환됩니다. `fmt=` 다음과 일치하지 않음 *`profile`*.

모두 *`renderIntent`* 및 *`blackpointComp`* 지정된 ICC 프로파일과 호환하지 않는 경우에는 무시됩니다.

CMYK 출력 장치 프로필은 다른 렌더링 의도를 지원할 가능성이 높습니다.

## 기본값 {#section-bbd3206fdcac4dc48a08fc9eba14fc90}

색상 관리가 활성화된 경우 및 `icc=` 을 지정하지 않으면 서버는 출력 프로필로 변환된 이미지를 전달합니다( `attribute::IccProfile*`)이 지정된 이미지 유형과 일치함 `fmt=`.

지정하지 않으면 *`renderIntent`* 다음에서 상속: `attribute::IccRenderIntent`, 및 *`blackpointComp`* 다음에서 상속: `attribute::IccBlackPointCompensation`.

## 참조 {#section-37ef83149fd74345956a98f633cc0294}

[색상 관리](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-color-management.md#concept-7bac7c2c41be42c1b301eae80abe6b8d), [attribute::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127), [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f), [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0)
