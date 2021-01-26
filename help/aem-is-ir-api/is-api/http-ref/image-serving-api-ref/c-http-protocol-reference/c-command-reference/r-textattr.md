---
description: 텍스트 레이어 속성입니다. rtf 명령으로 사용할 수 없는 텍스트 레이어의 추가 특성을 지정합니다.
seo-description: 텍스트 레이어 속성입니다. rtf 명령으로 사용할 수 없는 텍스트 레이어의 추가 특성을 지정합니다.
seo-title: textAttr
solution: Experience Manager
title: textAttr
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 07b3d263-2ed6-4363-83e1-3b841e9967c5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 1%

---


# textAttr{#textattr}

텍스트 레이어 속성입니다. rtf 명령으로 사용할 수 없는 텍스트 레이어의 추가 특성을 지정합니다.

` textAttr= *``*[, *``*[, *``*[, *`resantiAliasingresModewordWrap`*]]]`

<table id="simpletable_0072BF7DF52B4959A14EDEF60A6EBDEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> res  </span> </span> </p> </td> 
  <td class="stentry"> <p>글꼴 크기를 변경하지 않고 텍스트 레이어의 크기를 조정할 수 있는 방법을 제공합니다. 해상도 값이 높을수록 캔버스 크기를 기준으로 렌더링된 텍스트의 크기가 커집니다.값이 작을수록 텍스트 크기가 줄어듭니다. 인치당 점의 텍스트 해상도(0보다 큼) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 앤티 앨리어스  </span> </span> </p> </td> 
  <td class="stentry"> <p>텍스트 렌더링 엔진에서 사용하는 앤티 앨리어스 모드를 제어합니다. </p> <p> <span class="codeph"> off | 정상 | 또렷하 | sharp | strong | 매끄럽게  </span> </p> <p> 
    <table id="simpletable_AE2331118FCA4BC7877233E287CED6A4"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 꺼짐 </span> </p> </td> 
      <td class="stentry"> <p>텍스트 앤티 앨리어스 기능을 비활성화합니다. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 규범  </span> </p> </td> 
      <td class="stentry"> <p>표준 텍스트 앤티 앨리어스 모드를 활성화합니다(기본값). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 선명하  </span> </p> </td> 
      <td class="stentry"> <p>Photoshop 앤티 앨리어싱 모드 <span class="codeph"> 선명하게 </span>( <span class="codeph"> textPs= </span>만 해당)를 선택합니다. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 날카로운  </span> </p> </td> 
      <td class="stentry"> <p>Photoshop 앤티 앨리어스 모드 <span class="codeph"> sharp </span>( <span class="codeph"> textPs= </span>만 해당)를 선택합니다. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 강력함 </span> </p> </td> 
      <td class="stentry"> <p>Photoshop 앤티 앨리어스 모드 <span class="codeph"> 강력한 </span>( <span class="codeph"> textPs= </span>만 해당)를 선택합니다. </p> </td> 
     </tr> 
    </table> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> resMode </span> </span> </p> </td> 
  <td class="stentry"> <p>텍스트를 렌더링할 때 사용되는 모양을 제어합니다. </p> <p> <span class="codeph"> fixedRes | autoRes | maxRes  </span> </p> <p> 
    <table id="simpletable_2CFC06DB37154C7C92614FDF7A818DB5"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> fixedRes  </span> </p> </td> 
      <td class="stentry"> <p>지정된 해상도를 사용합니다. </p> <p>텍스트를 합성 캔버스에 상대적인 정확한 크기로 렌더링하는 경우에 사용합니다. 텍스트 상자가 너무 작은 경우 텍스트가 레이어 크기(지정된 경우)로 잘릴 수 있습니다. 이것은 <span class="codeph"> textPs= </span>에서 지원하는 유일한 <span class="varname"> resMode </span> 옵션입니다. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> autoRes  </span> </p> </td> 
      <td class="stentry"> <p>레이어 사각형을 텍스트로 칠하기 위해 해상도를 자동으로 조정합니다. </p> <p>텍스트 상자가 잘릴 위험이 없이 가능한 한 많이 채워지도록 텍스트 크기를 자동으로 조정하는 데 사용합니다. 줄 바꿈이 활성화된 경우 최종 해상도로 텍스트가 줄 바꿈될 수 있습니다. <span class="varname"> autoRes </span> 를 선택한 경우  <span class="codeph"> res </span> 는 무시됩니다. <span class="codeph"> textPs= </span>에서 지원되지 않습니다. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> maxRes  </span> </p> </td> 
      <td class="stentry"> <p>지정된 해상도를 사용합니다.필요한 경우 레이어 사각형으로 텍스트가 잘리지 않도록 줄입니다. </p> <p>클리핑이 발생하지 않는 한 지정된 해상도에서 텍스트를 렌더링하는 데 사용합니다. 클리핑의 경우 모든 텍스트가 텍스트 상자 안에 완전히 포함되도록 해상도가 자동으로 감소됩니다. 줄 바꿈이 활성화된 경우 최종 해상도로 텍스트가 줄 바꿈될 수 있습니다. <span class="codeph"> textPs= </span>에서 지원되지 않습니다. </p> </td> 
     </tr> 
    </table> </p> <p>텍스트 레이어 크기가 size=로 지정되지 않았거나 너비만 지정된 경우 'autoRes' 및 'maxRes' 설정이 무시되고 지정된 해상도가 텍스트를 렌더링하는 데 사용됩니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> wordWrap  </span> </span> </p> </td> 
  <td class="stentry"> <p>래핑 모드를 지정합니다. </p> <p> <span class="codeph"> 감싸기 | noWrap | nbWrap  </span> </p> <p> 
    <table id="simpletable_FF2510E029EC41E29BC30D9FC2923EA3"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> noWrap  </span> </p> </td> 
      <td class="stentry"> <p>단어 줄 바꿈을 사용하지 않습니다. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 줄바꿈 </span> </p> </td> 
      <td class="stentry"> <p>표준 줄 바꿈을 활성화합니다. </p> <p>필요한 경우 긴 단어를 구분합니다. <span class="codeph"> textPs= </span> 는  <span class="codeph"> 줄바꿈만 지원합니다 </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nbWrap  </span> </p> </td> 
      <td class="stentry"> <p>단어 줄 바꿈을 사용하지 않도록 설정합니다. </p> <p>마지막에 잘리더라도 단어를 끊지 마십시오. 일반적으로 긴 단어가 끊어지지 않도록 <span class="codeph"> autoRes </span> 또는 <span class="codeph"> maxRes </span>와 함께 사용됩니다. </p> </td> 
     </tr> 
    </table> </p> <p><span class="codeph"> 모두 단어 경계 및 하이픈에 </span> 및 <span class="codeph"> 자동 줄 바꿈을 추가합니다.</span> </p> </td> 
 </tr> 
</table>

## 속성 {#section-114ca0b8585b403c873e2251478ad1d5}

텍스트 레이어 속성입니다. 이미지, 단색 및 효과 레이어에서 무시됩니다. `layer=comp`에 대해 지정된 경우 `layer=0`에 적용됩니다.

## 기본값 {#section-855230f5330b4afc8a933f00a1ed4612}

`textAttr=72,norm,fixedRes,wrap`

## 참조 {#section-68b0d2e2d0474e2097a9331ae272c224}

[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) ,  [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767),  [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
