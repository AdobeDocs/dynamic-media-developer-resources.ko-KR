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
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 1%

---


# 수량화{#quantize}

색상 양자화 GIF 출력 변환의 색상 양자화 특성을 지정합니다.

` quantize= *``*[, *``*[, *``*[, *`typedthernumColorscolorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> type  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptive|web|mac}  </span> 팔레트 유형 </p> <p>사전 정의된 팔레트를 선택하려면 ' <span class="codeph"> web </span>' 또는 ' <span class="codeph"> mac </span>'을 선택하고, 이미지에 대한 최적의 팔레트를 계산하려면 ' <span class="codeph"> adaptive </span>'로 설정합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 디더  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {diffuse|off} 디더링  </span> 옵션 </p> <p>디더링을 비활성화하려면 Floyd-Steinberg 오류 확산의 경우 'diffuse' 또는 'off'를 선택합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> </p> </td> 
  <td class="stentry"> <p>' <span class="codeph"> 응용 </span>' 팔레트에 포함된 출력 색상(정수) 수입니다. </p> <p> <span class="codeph"> <span class="varname"> numColors는 2에서 256 사이여야  </span> </span> 합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList  </span> </span> </p> </td> 
  <td class="stentry"> <p>16진수6 형식의 강제 RGB 색상의 쉼표로 구분된 목록. ' <span class="codeph"> 응용 </span>' 팔레트에 포함할 강제 색상을 지정할 수 있습니다. 지정된 색상 수가 <span class="codeph"> numColors </span>보다 작으면 이미지 내용에 따라 추가 색상이 계산됩니다. </p> <p><span class="codeph"> fmt=gif </span> 또는 <span class="codeph"> fmt=gif-alpha </span>인 경우에만 사용됩니다. 그렇지 않으면 무시됩니다. <span class="codeph"> <span class="varname"> colorList </span> </span>에 지정된 색상은 16진수6 형식의 RGB 값이어야 합니다( <span class="codeph"> color </span> 참조).다른 색상 지정자는 허용되지 않습니다. </p> </td> 
 </tr> 
</table>

## 기본값 {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## 예 {#section-b3a979dc9ae3459baa093bf17310988f}

디더링 없이 &#39; `web`&#39; 팔레트를 사용하여 GIF 축소판을 생성합니다.

[!DNL http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off]

이미지를 키 색상 투명도가 있는 두 가지 색조 GIF로 변환하고 색상을 흑백으로 강제 적용합니다.

[!DNL http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff]
