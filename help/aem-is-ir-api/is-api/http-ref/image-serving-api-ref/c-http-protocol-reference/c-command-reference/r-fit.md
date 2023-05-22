---
title: 맞춤
description: 응답 이미지 맞춤 모드입니다. wid= 및 hei=로 응답 크기를 지정하고 scl=이 없는 경우 응답 이미지로 복합 이미지의 크기를 조정하는 데 사용되는 배율 계수를 계산하는 방법을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d2939f86-5dab-471d-ba59-70d91ae1e4fd
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 1%

---

# 맞춤{#fit}

응답 이미지 맞춤 모드입니다. wid= 및 hei=로 응답 크기를 지정하고 scl=이 없는 경우 응답 이미지로 복합 이미지의 크기를 조정하는 데 사용되는 배율 계수를 계산하는 방법을 지정합니다.

` fit= *`모드`*, *`고급`*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 모드 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 맞춤|제한|자르기|줄바꿈|늘리기|vfit </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 고급 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
 </tr> 
</table>

모드 옵션에 대한 다음 설명에서 다음과 같이 가정합니다. *`xScale`* 는 응답 이미지 너비에 대한 합성 이미지 너비의 비율입니다. *`yScale`* 응답 이미지 높이에 대한 합성 이미지 높이의 비율입니다.

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
   <td colname="col2"> <p>이미지가 할당된 공간에 맞게 합성 이미지 크기 조절 <span class="codeph"> wid= </span> 및 <span class="codeph"> hei= </span>, 공백 최소화 및 자르기 없음. 응답 이미지의 정확한 크기를 <span class="codeph"> wid= </span> 및 <span class="codeph"> hei= </span>. 중 작은 <span class="varname"> xScale </span> 및 <span class="varname"> yScale </span> 이 적용됩니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 제한 </span> </p> </td> 
   <td colname="col2"> <p>다음과 같이 합성 이미지 크기 조절 <span class="codeph"> 맞춤 </span> 할당된 공간에 맞게 조정 <span class="codeph"> wid= </span> 및 <span class="codeph"> hei= </span>: 실제 응답 이미지는 <span class="codeph"> wid= </span> 및 <span class="codeph"> hei= </span> 공백을 사용하지 않습니다. 중 작은 <span class="varname"> xScale </span> 및 <span class="varname"> yScale </span> 이 적용됩니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 자르기 </span> </p> </td> 
   <td colname="col2"> <p>자르기 작업을 최소화하고 공백을 사용하지 않고 전체 응답 이미지를 채우도록 합성 이미지의 비율을 조정합니다. 다음보다 큰 <span class="varname"> xScale </span> 및 <span class="varname"> yScale </span> 이 적용됩니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 줄바꿈 </span> </p> </td> 
   <td colname="col2"> <p>다음과 같이 합성 이미지 크기 조절 <span class="codeph"> 자르기 </span> 전체 응답 이미지를 포함하지만 실제 응답 이미지는 <span class="codeph"> wid= </span> 및 <span class="codeph"> hei= </span> 자르기를 방지합니다. 다음보다 큰 <span class="varname"> xScale </span> 및 <span class="varname"> yScale </span>이 적용됩니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 구간 </span> </p> </td> 
   <td colname="col2"> <p>자르기 없이 공백 없이 전체 응답 이미지를 채우도록 x와 y에서 합성 이미지의 비율을 독립적으로 조정합니다. 이렇게 하면 일반적으로 이미지의 종횡비가 변경됩니다. <span class="varname"> xScale </span> 는 수평 크기 조절에 사용되며 <span class="varname"> yScale </span> 세로 비율 조정 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> hfit </span> </p> </td> 
   <td colname="col2"> <p>적용 <span class="varname"> xScale </span> 위쪽과/또는 아래쪽에 자르기 또는 공백을 사용하여 이미지를 가로로 조입니다. 특수 응용 프로그램에 유용합니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vfit </span> </p> </td> 
   <td colname="col2"> <p>적용 <span class="varname"> yScale </span> 왼쪽 및/또는 오른쪽에 자르기 또는 공백을 사용하여 이미지를 수직으로 조입니다. 특수 응용 프로그램에 유용합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

설정 *`upscale`* 업스케일링을 허용하려면 &#39;1&#39;로 설정하고, 제한을 허용하려면 &#39;0&#39;으로 설정합니다. *`xScale`*및 *`yScale`* 1:1로 제한. 업스케일링이 비활성화되면, 합성 이미지가 응답 이미지보다 작은 경우 추가 공백이 존재할 수 있다.

자르기 및 공백은 기본적으로 가운데로 표시되며, 다음과 같이 위치를 제어할 수 있습니다. `align=`. 공백 채우기의 색상 및 불투명도는 다음 방법으로 결정됩니다. `bgc=`.

## 속성 {#section-6d7a5a7e18434bca9bc2fdb236af8909}

속성 보기. 현재 레이어 설정에 관계없이 적용됩니다. 하나 이상의 `wid=` 또는 `hei=` 을 지정해야 합니다. 지정하지 않으면 오류가 반환됩니다. `wid=` 및 `hei=` 설명된 대로 맞춤 모드가 작동하도록 지정해야 합니다. 다음과 같은 경우 오류가 반환됩니다. `req=tmb` 도 지정됩니다.

## 기본값 {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## 참조 {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [정렬=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
