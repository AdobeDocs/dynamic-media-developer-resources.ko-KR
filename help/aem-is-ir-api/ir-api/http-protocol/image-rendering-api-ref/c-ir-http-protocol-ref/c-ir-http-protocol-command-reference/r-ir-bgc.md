---
title: bgc
description: 배경색. 색상 적용 가능한 텍스처와 디캘의 빼기 색상을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9ac6517e-b9c3-48d9-97ac-d8aa65a8ba46
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 6%

---

# bgc {#bgc}

배경색. 색상 적용 가능한 텍스처와 디캘의 빼기 색상을 지정합니다.

`bgc= *[!DNL color]*`

<table id="simpletable_131302355CAB4900A7B45FED903A1AAD" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p><span class="+ topic/keyword sw-d/varname varname"> color</span> </p> </td> 
  <td class="- topic/stentry stentry"> <p>RGB 또는 회색 색상 값. </p></td> 
 </tr> 
</table>

이미지 렌더링의 텍스쳐 색상화 알고리즘은 간단합니다. 구성 요소는 다음과 같습니다 `bgc=` 텍스처 픽셀 값에서 빼집니다. `color=` 가 추가되고 마지막으로 결과가 클립됩니다. `0,0,0` 및 `255,255,255`.

텍스쳐 색상화의 일반적인 사용 방법은 다음 값을 사용하는 것입니다 `bgc=` 텍스처 이미지에서 가장 중요하거나 강력한 색상을 사용할 수 있습니다. Dynamic Media 이미지 작성은 합리적인 추출을 수행하는 반자동 도구를 제공합니다 `bgc=` 텍스처 이미지의 색상 값.

텍스처 재질이 텍스처가 불가능한 비네팅 객체에 적용되면 `bgc=` 이 전경 색상으로 적용된 경우 `color=` 이 지정되지 않았습니다.

## 속성 {#section-b2db6f147d7f443ba9f671de04c2ef19}

재료 속성입니다. 고색 및 캐비닛 자료에 의해 무시됨.

## 기본값 {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor` 자재가 카탈로그 항목을 기반으로 하는 경우, 그렇지 않으면 `bgc=808080` (중성 회색)

## 예 {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

텍스처가 가장 큰 RGB 색상 120,34,193인 의류 원단에 색상을 지정합니다.

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## 참조 {#section-de9958dd63a742b4b5d780c59a57da33}

[카탈로그::BaseColor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8) , [color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)
