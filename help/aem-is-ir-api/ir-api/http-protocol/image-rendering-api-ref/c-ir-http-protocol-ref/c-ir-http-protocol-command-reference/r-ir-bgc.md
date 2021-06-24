---
description: 배경색. 색상 적용 가능한 텍스처와 디캘의 빼기 색상을 지정합니다.
solution: Experience Manager
title: bgc
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 9ac6517e-b9c3-48d9-97ac-d8aa65a8ba46
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 6%

---

# bgc{#bgc}

배경색. 색상 적용 가능한 텍스처와 디캘의 빼기 색상을 지정합니다.

`bgc= *[!DNL color]*`

<table id="simpletable_131302355CAB4900A7B45FED903A1AAD" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p><span class="+ topic/keyword sw-d/varname varname"> color</span> </p> </td> 
  <td class="- topic/stentry stentry"> <p>RGB 또는 회색 색상 값입니다. </p></td> 
 </tr> 
</table>

이미지 렌더링의 텍스쳐 색상 지정 알고리즘은 매우 간단합니다. `bgc=`의 구성 요소 값은 텍스쳐 픽셀의 값에서 뺀 후 `color=`이 추가되고, 결과는 `0,0,0` 및 `255,255,255`에 클리핑됩니다.

텍스처 색상화를 일반적으로 사용하는 경우 `bgc=` 값이 텍스처 이미지에서 가장 중요하거나 우세한 색일 수 있습니다. Dynamic Media 이미지 작성은 텍스처 이미지에서 적절한 `bgc=` 색상 값을 추출하는 반자동 도구를 제공합니다.

텍스처 재료가 텍스트가 아닌 비네팅 개체에 적용되면 `color=`이(가) 지정되지 않은 경우 `bgc=`이 전경색으로 적용됩니다.

## 속성 {#section-b2db6f147d7f443ba9f671de04c2ef19}

재료 속성입니다. 고색 및 캐비닛 자료에 의해 무시됨.

## 기본값 {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor` 자재가 카탈로그 항목을 기반으로 하는 경우, 그렇지 않으면  `bgc=808080` (중립 회색)

## 예 {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

텍스처가 지배적인 RGB 색상 120,34,193인 의류 원단에 색상화:

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## 참조 {#section-de9958dd63a742b4b5d780c59a57da33}

[catalog::BaseColor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8) ,  [color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)
