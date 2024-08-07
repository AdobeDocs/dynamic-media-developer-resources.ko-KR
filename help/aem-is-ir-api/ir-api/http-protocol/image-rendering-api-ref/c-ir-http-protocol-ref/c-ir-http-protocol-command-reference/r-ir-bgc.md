---
title: bgc
description: 배경색입니다. 색상화 가능한 텍스처 및 데칼의 감색 색상을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9ac6517e-b9c3-48d9-97ac-d8aa65a8ba46
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 2%

---

# bgc {#bgc}

배경색입니다. 색상화 가능한 텍스처 및 데칼의 감색 색상을 지정합니다.

`bgc= *[!DNL color]*`

<table id="simpletable_131302355CAB4900A7B45FED903A1AAD" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p><span class="+ topic/keyword sw-d/varname varname"> 색상</span> </p> </td> 
  <td class="- topic/stentry stentry"> <p>RGB 또는 회색 색상 값입니다. </p></td> 
 </tr> 
</table>

이미지 렌더링의 텍스처 색상화 알고리즘은 간단합니다. 텍스처 픽셀 값에서 `bgc=`의 구성 요소 값을 빼고 `color=`을(를) 추가한 다음 최종적으로 결과가 `0,0,0` 및 `255,255,255`(으)로 잘립니다.

일반적인 텍스처 색상화의 경우 `bgc=` 값이 텍스처 이미지에서 가장 중요하거나 지배적인 색상일 수 있습니다. Dynamic Media 이미지 작성에서는 텍스처 이미지에서 합리적인 `bgc=` 색상 값을 추출하는 반자동 도구를 제공합니다.

질감이 아닌 비네팅 개체에 질감 재료를 적용할 경우 `color=`을(를) 지정하지 않으면 `bgc=`이(가) 전경색으로 적용됩니다.

## 속성 {#section-b2db6f147d7f443ba9f671de04c2ef19}

재질 속성입니다. 단색 및 캐비닛 소재에서 무시됩니다.

## 기본값 {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor` 자료가 카탈로그 항목을 기반으로 하는 경우, 그렇지 않으면 `bgc=808080`(중간 회색).

## 예 {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

120,34,193의 우세한 RGB 색상을 가진 의류 원단을 색상화합니다.

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## 참조 {#section-de9958dd63a742b4b5d780c59a57da33}

[카탈로그::BaseColor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8) , [색상=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)
