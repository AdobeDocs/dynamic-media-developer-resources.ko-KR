---
title: 맞춤
description: 응답 이미지 맞추기 모드입니다. wid= 및 hei= 및 scl= 로 응답 크기가 지정되지 않은 경우 복합 이미지를 응답 이미지로 스케일링하는 데 사용되는 배율 계수를 계산하는 방법을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d2939f86-5dab-471d-ba59-70d91ae1e4fd
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 2%

---

# 맞춤{#fit}

응답 이미지 맞추기 모드입니다. wid= 및 hei= 및 scl= 로 응답 크기가 지정되지 않은 경우 복합 이미지를 응답 이미지로 스케일링하는 데 사용되는 배율 계수를 계산하는 방법을 지정합니다.

` fit= *`모드`*, *`고급`*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 모드 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fit|constrain|crop|wrap|스트레치|hfit|vfit </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 고급 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
 </tr> 
</table>

모드 옵션에 대한 다음 설명에서 *`xScale`* 는 응답 이미지 너비와 합성 이미지 너비의 비율입니다 *`yScale`* 는 응답 이미지 높이에 대한 합성 이미지 높이의 비율입니다.

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
   <td colname="col2"> <p>합성 이미지를 <span class="codeph"> wid= </span> 및 <span class="codeph"> hei= </span>작은 공백 및 자르지 않고 응답 이미지의 크기가 <span class="codeph"> wid= </span> 및 <span class="codeph"> hei= </span>. 작은 <span class="varname"> xScale </span> 및 <span class="varname"> yScale </span> 이 적용됩니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 제한 </span> </p> </td> 
   <td colname="col2"> <p>다음과 같이 합성 이미지의 비율을 조정합니다 <span class="codeph"> fit </span> 그래서, <span class="codeph"> wid= </span> 및 <span class="codeph"> hei= </span>하지만 실제 응답 이미지는 <span class="codeph"> wid= </span> 및 <span class="codeph"> hei= </span> 공백은 피하려면 작은 <span class="varname"> xScale </span> 및 <span class="varname"> yScale </span> 이 적용됩니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 자르기 </span> </p> </td> 
   <td colname="col2"> <p>자르기를 최소화하고 공백을 제외하고 전체 응답 이미지를 채우도록 합성 이미지의 크기를 조정합니다. 큰 <span class="varname"> xScale </span> 및 <span class="varname"> yScale </span> 이 적용됩니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 줄바꿈 </span> </p> </td> 
   <td colname="col2"> <p>다음과 같이 합성 이미지의 비율을 조정합니다 <span class="codeph"> 자르기 </span> 전체 응답 이미지를 포함하지만 실제 응답 이미지는 <span class="codeph"> wid= </span> 및 <span class="codeph"> hei= </span> 자르기를 방지하려면 다음을 수행하십시오. 큰 <span class="varname"> xScale </span> 및 <span class="varname"> yScale </span>이 적용됩니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 스트레치 </span> </p> </td> 
   <td colname="col2"> <p>컴포지트 이미지를 x와 y로 독립적으로 확장하여 자르거나 공백을 사용하지 않고 전체 응답 이미지를 채웁니다. 이렇게 하면 일반적으로 이미지의 종횡비가 변경됩니다. <span class="varname"> xScale </span> 가로 크기 조절에 사용됩니다. <span class="varname"> yScale </span> 세로 크기 조절을 위해 사용됩니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 건달 </span> </p> </td> 
   <td colname="col2"> <p>적용 <span class="varname"> xScale </span> 이미지를 가로로 밀기 위해 위쪽 및/또는 아래쪽에서 자르거나 공백을 사용할 수 있습니다. 특수 응용 프로그램에 유용합니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vfit </span> </p> </td> 
   <td colname="col2"> <p>적용 <span class="varname"> yScale </span> 이미지를 세로로 맞추기 위해 왼쪽 및/또는 오른쪽에 자르거나 공백을 사용할 수 있습니다. 특수 응용 프로그램에 유용합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

설정 *`upscale`* 업스케일링을 허용하거나 &#39;0&#39;으로 설정하면 *`xScale`*및 *`yScale`* 1:1로 제한됩니다. 업스케일링을 사용하지 않도록 설정하면 합성 이미지가 응답 이미지보다 작은 경우 추가 공백이 있을 수 있습니다.

자르기와 공백은 기본적으로 가운데에 표시됩니다. 그들의 위치는 `align=`. 공백 채우기의 색상 및 불투명도는 `bgc=`.

## 속성 {#section-6d7a5a7e18434bca9bc2fdb236af8909}

속성 보기. 현재 레이어 설정에 관계없이 적용됩니다. 하나 이상 `wid=` 또는 `hei=` 또한 지정해야 하며, 그렇지 않으면 오류가 반환됩니다. 둘 다 `wid=` 및 `hei=` 적합한 모드가 설명된 대로 동작하도록 지정해야 합니다. 다음 경우에 오류가 반환됩니다 `req=tmb` 도 지정됩니다.

## 기본값 {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## 참조 {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [정렬=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
