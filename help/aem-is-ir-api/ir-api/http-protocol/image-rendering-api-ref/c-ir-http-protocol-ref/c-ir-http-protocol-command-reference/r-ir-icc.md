---
title: icc
description: 출력 색상 프로파일.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39b25f7c-ed3c-4132-8241-e7f3aab07b00
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 1%

---

# icc{#icc}

출력 색상 프로파일.

icc= *`profile`**`renderIntent`*[,*`blackpointComp`*]]

<table id="simpletable_DF1914FD351E4F2BA61372A52F0CFFBF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 프로필</span></span> </p></td> 
  <td class="stentry"> <p>ICC 색상 프로파일. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent </span> </span> </p></td> 
  <td class="stentry"> <p>인식 | 상대적 | 채도 | 절대 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span> </span> </p></td> 
  <td class="stentry"> <p>활성화하려면 1을 사용하고, 검은 점 보상을 비활성화하려면 0을 사용합니다. </p></td> 
 </tr> 
</table>

*`profile`* 렌더링된 이미지가 작업 프로필과 다른 경우 변환해야 하는 출력 색상 공간 프로필을 지정합니다. *`profile`*&#x200B;은(는) 이미지 카탈로그 또는 기본 카탈로그의 ICC 프로필 맵에 정의된 올바른 `icc::Name`이거나 프로필 파일에 대한 상대 경로여야 합니다(일반적으로 [!DNL `.icc`] 또는 [!DNL `.icm`] 접미사 사용).

>[!NOTE]
>
>*`profile`*&#x200B;에는 HTTP로 인코딩된 경우에도 &#39;,&#39; 문자가 포함되지 않을 수 있습니다.

*`renderIntent`* 기본 렌더링 의도를 재정의할 수 있습니다.

*`blackpointComp`* 출력 프로필에서 이 기능을 지원하는 경우 검은 점 보상을 사용합니다.

>[!NOTE]
>
>일부 색상 변환에서는 모든 *`renderIntent`* 및 *`blackpointComp`* 선택을 지원하지 않습니다. 일반적으로 이러한 설정은 ICC 출력 프로파일이 프린터 또는 모니터와 같은 출력 장치를 특성화하는 경우에만 적용됩니다. 또한 일부 ICC 출력 프로필은 모든 *`renderIntent`* 선택을 지원하지 않습니다.

## 속성 {#section-b4042623a8ea40248c11b2153e5906b1}

요청 내의 어느 곳에서든 발생할 수 있습니다. `fmt=`(으)로 지정된 이미지 형식이 *`profile`*&#x200B;과(와) 일치하지 않으면 오류가 반환됩니다.

지정된 ICC 프로필과 호환되지 않으면 *`renderIntent`* 및 *`blackpointComp`*&#x200B;이(가) 모두 무시됩니다.

CMYK 출력 장치 프로필은 다른 렌더링 의도를 지원할 가능성이 높습니다.

## 기본값 {#section-bbd3206fdcac4dc48a08fc9eba14fc90}

색상 관리가 활성화되어 있고 `icc=`이(가) 지정되지 않은 경우 서버는 `attribute::IccProfile*`에 지정된 이미지 유형과 일치하는 출력 프로필(`fmt=`)로 변환된 이미지를 전달합니다.

지정하지 않으면 *`renderIntent`*&#x200B;은(는) `attribute::IccRenderIntent`에서 상속되고 *`blackpointComp`*&#x200B;은(는) `attribute::IccBlackPointCompensation`에서 상속됩니다.

## 참조 {#section-37ef83149fd74345956a98f633cc0294}

[색상 관리](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-color-management.md#concept-7bac7c2c41be42c1b301eae80abe6b8d), [특성::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127), [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f), [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [특성::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [특성::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0)
