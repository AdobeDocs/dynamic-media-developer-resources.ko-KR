---
description: 색상 양자화 GIF 출력 변환의 색상 양자화 특성을 지정합니다.
seo-description: 색상 양자화 GIF 출력 변환의 색상 양자화 특성을 지정합니다.
seo-title: 수량화
solution: Experience Manager
title: 수량화
topic: Scene7 Image Serving - Image Rendering API
uuid: 624cdc45-51f2-4b18-a658-311770974521
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 수량화{#quantize}

색상 양자화 GIF 출력 변환의 색상 양자화 특성을 지정합니다.

` quantize= *`typedithernumColorscolorList`*[, *``*[, *``*[, *``*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 유형 </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptive|web|mac} </span> 팔레트 유형 </p> <p>' <span class="codeph"> web </span>' 또는 ' <span class="codeph"> mac'을 선택하여 사전 정의된 팔레트를 선택하거나, ' </span>adaptive <span class="codeph"> </span>'로 설정하여 이미지에 대한 최적의 팔레트를 계산합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 디더 </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {diffuse|off} </span> 디더링 옵션 </p> <p>Floyd-Steinberg 오류 확산의 경우 'diffuse' 또는 'off'를 선택하여 디더링을 비활성화합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> num <span class="varname"> Colors </span></span> </p> </td> 
  <td class="stentry"> <p>' <span class="codeph"> 응용 </span>' 팔레트에 포함된 출력 색상(정수)의 수입니다. </p> <p> <span class="codeph"> num <span class="varname"> Colors </span> 는 2에서 256 사이여야 </span> 합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 색상 <span class="varname"> 목록 </span></span> </p> </td> 
  <td class="stentry"> <p>16진수6 형식의 강제 RGB 색상의 쉼표로 구분된 목록. ' <span class="codeph"> 응용 </span>' 팔레트에 포함되도록 강제 색상을 지정할 수 있습니다. 지정된 색상 수가 <span class="codeph"> num Colors보다 적은 </span>경우 이미지 컨텐츠를 기반으로 추가 색상이 계산됩니다. </p> <p>fmt=gif <span class="codeph"> 또는 </span> fmt=gif-alpha인 경우에만 <span class="codeph"> </span>사용됩니다. 그렇지 않으면 무시됩니다. colorList로 지정된 <span class="codeph"> 색상은 <span class="varname"> 16진수6 형식의 RGB 값이어야 </span> 합니다(색상 </span> <span class="codeph"> </span>참조).다른 색상 지정자는 허용되지 않습니다. </p> </td> 
 </tr> 
</table>

## 기본값 {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## 예 {#section-b3a979dc9ae3459baa093bf17310988f}

디더링 없이 &#39; `web`&#39; 팔레트를 사용하여 GIF 축소판을 생성합니다.

[!DNL http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off]

이미지를 키 색상 투명도가 있는 양방향 GIF로 변환하고 색상을 흑백으로 강제 적용합니다.

[!DNL http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff]
