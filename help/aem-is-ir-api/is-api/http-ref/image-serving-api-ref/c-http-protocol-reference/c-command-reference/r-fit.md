---
description: 응답 이미지 맞추기 모드. wid= 및 hei= 및 scl=로 응답 크기가 지정되지 않은 경우 복합 이미지를 응답 이미지로 크기 조절하는 데 사용되는 비율 인수를 계산하는 방법을 지정합니다.
seo-description: 응답 이미지 맞추기 모드. wid= 및 hei= 및 scl=로 응답 크기가 지정되지 않은 경우 복합 이미지를 응답 이미지로 크기 조절하는 데 사용되는 비율 인수를 계산하는 방법을 지정합니다.
seo-title: 맞춤
solution: Experience Manager
title: 맞춤
topic: Scene7 Image Serving - Image Rendering API
uuid: 669fe757-f3a1-4cd4-b46c-6fbe5a039ce0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 2%

---


# 맞춤{#fit}

응답 이미지 맞추기 모드. wid= 및 hei= 및 scl=로 응답 크기가 지정되지 않은 경우 복합 이미지를 응답 이미지로 크기 조절하는 데 사용되는 비율 인수를 계산하는 방법을 지정합니다.

` fit= *``*, *`중재`*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> mode  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fit|constrict|crop|wrap|늘리기|hfit|vfit  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 확대  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
 </tr> 
</table>

모드 옵션에 대한 다음 설명에서 *`xScale`*&#x200B;은 응답 이미지 너비에 대한 합성 이미지 너비의 비율이고 *`yScale`*&#x200B;은 응답 이미지 높이에 대한 합성 이미지 높이의 비율이라고 가정합니다.

<table id="table_33408ECA9D164AFAA249F8589060545E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 정의 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 맞춤 </span> </p> </td> 
   <td colname="col2"> <p>합성 이미지가 <span class="codeph"> wid= </span> 및 <span class="codeph"> hei= </span>로 할당된 공간에 맞게 조절되도록 크기를 조절하고 공백을 줄이고 잘라내지 않습니다. 응답 이미지의 크기는 <span class="codeph"> wid= </span> 및 <span class="codeph"> hei= </span>로 정확히 지정됩니다. <span class="varname"> xScale </span> 및 <span class="varname"> yScale </span> 중 작은 값이 적용됩니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 제한  </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">과(와) 같은 합성 이미지를 </span>에 맞추면 <span class="codeph"> wid= </span> 및 <span class="codeph"> hei= </span>와 함께 할당된 공간에 맞게 조정되지만 실제 응답 이미지는 <span class="codeph"> witd= </span> 및 <span class="codeph"> hei= </span>로 지정한 것보다 작아야 공백을 방지할 수 있습니다. <span class="varname"> xScale </span> 및 <span class="varname"> yScale </span> 중 작은 값이 적용됩니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 자르기 </span> </p> </td> 
   <td colname="col2"> <p>자르기를 최소화하고 공백은 제외하고 전체 응답 이미지를 채우도록 합성 이미지의 크기를 조정합니다. <span class="varname"> xScale </span> 및 <span class="varname"> yScale </span> 중 큰 값이 적용됩니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 줄바꿈 </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 자르기 </span>와 같은 합성 이미지의 크기를 조절하여 전체 응답 이미지를 덮지만, 실제 응답 이미지는 <span class="codeph"> wid= </span> 및 <span class="codeph"> hei= </span>로 지정한 것보다 더 커서 자르기를 방지할 수 있습니다. <span class="varname"> xScale </span> 및 <span class="varname"> yScale </span>의 큰 부분이 적용됩니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 스트레치  </span> </p> </td> 
   <td colname="col2"> <p>합성 이미지를 x 및 y에 개별적으로 크기 조정하여 자르기 작업 없이 전체 응답 이미지를 채웁니다. 이때 공백은 없습니다. 일반적으로 이미지의 종횡비가 변경됩니다. <span class="varname"> xScale </span> 은 가로 비율 및  <span class="varname"> yScale </span> 을 세로 비율 조정에 사용합니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> hfit  </span> </p> </td> 
   <td colname="col2"> <p>위쪽 및/또는 아래쪽의 자르기 또는 공백과 함께 <span class="varname"> xScale </span>을 적용하여 이미지를 가로로 밀도록 합니다. 특수 응용 프로그램에 유용합니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vfit  </span> </p> </td> 
   <td colname="col2"> <p>이미지를 세로로 맞추기 위해 <span class="varname"> yScale </span>을 적용하여 왼쪽 및/또는 오른쪽에 자르거나 공백이 있을 수 있습니다. 특수 응용 프로그램에 유용합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

업스케일링을 허용하려면 *`upscale`*&#x200B;을 &#39;1&#39;로 설정하고, *`xScale`*과 *`yScale`*&#x200B;를 1:1로 제한하도록 &#39;0&#39;으로 설정합니다. 업스케일링을 비활성화하면 합성 이미지가 응답 이미지보다 작으면 추가 공백이 있을 수 있습니다.

자르기와 공백은 기본적으로 가운데에 표시됩니다.해당 위치는 `align=`으로 제어할 수 있습니다. 공백 채우기의 색상 및 불투명도는 `bgc=`으로 결정됩니다.

## 속성 {#section-6d7a5a7e18434bca9bc2fdb236af8909}

속성을 봅니다. 현재 레이어 설정에 관계없이 적용됩니다. `wid=` 또는 `hei=` 중 하나 이상을 지정해야 하며, 그렇지 않으면 오류가 반환됩니다.맞춤 모드가 설명대로 작동하도록 `wid=` 및 `hei=` 모두를 지정해야 합니다. `req=tmb`도 지정되면 오류가 반환됩니다.

## 기본값 {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## 참조 {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [정렬=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
