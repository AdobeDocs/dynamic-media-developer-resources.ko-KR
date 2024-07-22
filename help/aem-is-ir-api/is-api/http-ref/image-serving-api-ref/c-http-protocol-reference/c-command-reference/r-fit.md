---
title: 맞춤
description: 응답 이미지 맞춤 모드입니다. wid= 및 hei=로 응답 크기를 지정하고 scl=이 없는 경우 응답 이미지로 복합 이미지의 크기를 조정하는 데 사용되는 배율 계수를 계산하는 방법을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d2939f86-5dab-471d-ba59-70d91ae1e4fd
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 1%

---

# 맞춤{#fit}

응답 이미지 맞춤 모드입니다. wid= 및 hei=로 응답 크기를 지정하고 scl=이 없는 경우 응답 이미지로 복합 이미지의 크기를 조정하는 데 사용되는 배율 계수를 계산하는 방법을 지정합니다.

` fit= *`모드`*, *`업그레이드`*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 모드 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 맞춤|제한|자르기|줄바꿈|hfit|vfit </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 확장 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
 </tr> 
</table>

모드 옵션에 대한 다음 설명에서, *`xScale`*&#x200B;은(는) 합성 이미지 폭과 응답 이미지 폭의 비율이고 *`yScale`*&#x200B;은(는) 합성 이미지 높이와 응답 이미지 높이의 비율이라고 가정한다.

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
   <td colname="col2"> <p>공백 수를 최소화하고 자르기 없이 <span class="codeph"> wid= </span> 및 <span class="codeph"> hei= </span>(으)로 할당된 공간에 맞도록 합성 이미지의 크기를 조정합니다. 응답 이미지의 크기가 <span class="codeph"> wid= </span> 및 <span class="codeph"> hei= </span>(으)로 지정되었습니다. <span class="varname"> xScale </span> 및 <span class="varname"> yScale </span> 중 작은 값이 적용됩니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 제한 </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> wid= </span> 및 <span class="codeph"> hei= </span>이(가) 할당된 공간에 맞도록 <span class="codeph"> fit </span>과(와) 같은 합성 이미지의 크기를 조정하지만 공백을 방지하기 위해 실제 응답 이미지가 <span class="codeph"> wid= </span> 및 <span class="codeph"> hei= </span>에 지정된 것보다 작을 수 있습니다. <span class="varname"> xScale </span> 및 <span class="varname"> yScale </span> 중 작은 값이 적용됩니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 자르기 </span> </p> </td> 
   <td colname="col2"> <p>자르기 작업을 최소화하고 공백을 사용하지 않고 전체 응답 이미지를 채우도록 합성 이미지의 비율을 조정합니다. <span class="varname"> xScale </span> 및 <span class="varname"> yScale </span> 중 큰 값이 적용됩니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 줄 바꿈 </span> </p> </td> 
   <td colname="col2"> <p>전체 응답 이미지를 포함하도록 합성 이미지 크기를 <span class="codeph"> 자르기 </span>과(와) 같이 조정하지만 자르기 방지를 위해 실제 응답 이미지가 <span class="codeph"> wid= </span> 및 <span class="codeph"> hei= </span>(으)로 지정된 크기보다 클 수 있습니다. <span class="varname"> xScale </span> 및 <span class="varname"> yScale </span> 중 큰 값이 적용됩니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 스트레치 </span> </p> </td> 
   <td colname="col2"> <p>자르기 없이 공백 없이 전체 응답 이미지를 채우도록 x와 y에서 합성 이미지의 비율을 독립적으로 조정합니다. 이렇게 하면 일반적으로 이미지의 종횡비가 변경됩니다. <span class="varname"> xScale </span>은(는) 가로 크기 조절에 사용되며 <span class="varname"> yScale </span>은(는) 세로 크기 조절에 사용됩니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> hfit </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> xScale </span>을(를) 적용하여 이미지를 가로로 촘촘하게 맞추고 위쪽과/또는 아래쪽에서 자르기 또는 공백을 사용할 수 있습니다. 특수 응용 프로그램에 유용합니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vfit </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> yScale </span>을(를) 적용하여 왼쪽 및/또는 오른쪽에 자르기 또는 공백을 사용하여 이미지를 세로로 조입니다. 특수 응용 프로그램에 유용합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`upscale`*&#x200B;을(를) &#39;1&#39;(으)로 설정하여 업스케일링을 허용하거나 &#39;0&#39;(으)로 설정하여 *`xScale`*및 *`yScale`*&#x200B;을(를) 1:1로 제한합니다. 업스케일링이 비활성화되면, 합성 이미지가 응답 이미지보다 작은 경우 추가 공백이 존재할 수 있다.

자르기 및 공백은 기본적으로 가운데에 있으며 `align=`을(를) 사용하여 위치를 제어할 수 있습니다. 공백 채우기의 색상 및 불투명도는 `bgc=`에 의해 결정됩니다.

## 속성 {#section-6d7a5a7e18434bca9bc2fdb236af8909}

속성 보기. 현재 레이어 설정에 관계없이 적용됩니다. `wid=` 또는 `hei=` 중 하나 이상을 지정해야 합니다. 그렇지 않으면 오류가 반환됩니다. 설명된 대로 맞춤 모드가 작동하려면 `wid=` 및 `hei=`을(를) 모두 지정해야 합니다. `req=tmb`도 지정되면 오류가 반환됩니다.

## 기본값 {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## 참조 {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
