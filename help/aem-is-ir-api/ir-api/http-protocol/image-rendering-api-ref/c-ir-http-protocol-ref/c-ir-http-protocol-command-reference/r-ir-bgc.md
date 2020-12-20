---
description: 배경색. 색상화할 수 있는 텍스처 및 디캘에 대해 빼기 색상을 지정합니다.
seo-description: 배경색. 색상화할 수 있는 텍스처 및 디캘에 대해 빼기 색상을 지정합니다.
seo-title: bgc
solution: Experience Manager
title: bgc
topic: Scene7 Image Serving - Image Rendering API
uuid: 551a0da8-dd1f-484a-bf7e-f4896370340a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 7%

---


# bgc{#bgc}

배경색. 색상화할 수 있는 텍스처 및 디캘에 대해 빼기 색상을 지정합니다.

`bgc= *[!DNL color]*`

<table id="simpletable_131302355CAB4900A7B45FED903A1AAD" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p><span class="+ topic/keyword sw-d/varname varname"> color</span> </p> </td> 
  <td class="- topic/stentry stentry"> <p>RGB 또는 회색 색상 값입니다. </p></td> 
 </tr> 
</table>

이미지 렌더링의 텍스처 색상화 알고리즘은 매우 간단합니다. 즉, `bgc=`의 구성 요소 값은 텍스처 픽셀의 값에서 빼고 `color=`이 추가되고 마지막으로 결과는 `0,0,0` 및 `255,255,255`에 클리핑됩니다.

텍스처 색상화를 일반적으로 사용하는 경우 `bgc=` 값이 텍스처 이미지에서 가장 중요하거나 우세한 색상이 될 수 있습니다. Scene7 이미지 작성은 텍스처 이미지에서 적절한 `bgc=` 색상 값을 추출하는 반자동 도구를 제공합니다.

텍스처 재질이 텍스처 비네팅 객체에 적용되면 `color=`이 지정되지 않은 경우 `bgc=`이 전경색으로 적용됩니다.

## 속성 {#section-b2db6f147d7f443ba9f671de04c2ef19}

재료 속성. 단색 및 캐비닛 재질로 무시됩니다.

## 기본값 {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor` 자료가 카탈로그 항목을 기반으로 하는 경우 그렇지 않은 경우  `bgc=808080` (중립 회색)

## 예 {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

텍스처에 기본 RGB 색상이 120,34,193인 의류 패브릭에 색상화:

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## 참조 {#section-de9958dd63a742b4b5d780c59a57da33}

[catalog::BaseColor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8) ,  [color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)
