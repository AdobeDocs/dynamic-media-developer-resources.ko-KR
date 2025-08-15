---
title: textAttr
description: 텍스트 레이어 특성입니다. rtf 명령으로 사용할 수 없는 텍스트 레이어의 추가 특성을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c8a3d2a-2524-436a-8bc7-60241af0fd17
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# textAttr{#textattr}

텍스트 레이어 특성입니다. rtf 명령으로 사용할 수 없는 텍스트 레이어의 추가 특성을 지정합니다.

` textAttr= *`res`*[, *`앤티앨리어싱`*[, *`resMode`*[, *`단어 줄바꿈`*]]]`

<table id="simpletable_0072BF7DF52B4959A14EDEF60A6EBDEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> res </span> </span> </p> </td> 
  <td class="stentry"> <p>글꼴 크기를 변경하지 않고 텍스트 레이어의 비율을 조정할 수 있는 수단을 제공합니다. 해상도 값이 높을수록 캔버스 크기에 상대적으로 렌더링된 텍스트의 크기가 커지고 값이 작을수록 텍스트 크기가 줄어듭니다. 인치당 도트 수(정수 0보다 큼)의 텍스트 해상도. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 앤티앨리어싱 </span> </span> </p> </td> 
  <td class="stentry"> <p>텍스트 렌더링 엔진에서 사용하는 앤티앨리어싱 모드를 제어합니다. </p> <p> <span class="codeph"> 해제 | 규범 | 파삭파삭하 | 예리하 | 강력함 | </span> 매끄럽게 </p> <p> 
    <table id="simpletable_AE2331118FCA4BC7877233E287CED6A4"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> / </span> </p> </td> 
      <td class="stentry"> <p>텍스트 앤티앨리어싱을 비활성화합니다. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 표준 </span> </p> </td> 
      <td class="stentry"> <p>표준 텍스트 앤티앨리어싱 모드를 활성화합니다(기본값). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 선명한 </span> </p> </td> 
      <td class="stentry"> <p>Photoshop 앤티앨리어싱 모드 <span class="codeph">을(를) 선택합니다. </span>이(가) 선명합니다(<span class="codeph"> textPs= </span>만). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 선명하게 </span> </p> </td> 
      <td class="stentry"> <p>Photoshop 앤티앨리어싱 모드 <span class="codeph"> 선명하게 </span>을(를) 선택하십시오(<span class="codeph"> textPs= </span>만). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 강력한 </span> </p> </td> 
      <td class="stentry"> <p>Photoshop 앤티앨리어싱 모드 <span class="codeph">의 강력한 </span>을(를) 선택하십시오(<span class="codeph"> textPs= </span>만). </p> </td> 
     </tr> 
    </table> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> resMode </span> </span> </p> </td> 
  <td class="stentry"> <p>텍스트를 렌더링할 때 레스가 사용되는 방법을 제어합니다. </p> <p> <span class="codeph"> fixedRes | autoRes | maxRes </span> </p> <p> 
    <table id="simpletable_2CFC06DB37154C7C92614FDF7A818DB5"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> fixedRes </span> </p> </td> 
      <td class="stentry"> <p>지정된 해상도를 사용합니다. </p> <p>텍스트가 합성된 캔버스에 비례하여 정확한 크기로 렌더링될 경우 를 사용합니다. 텍스트 상자가 너무 작으면 텍스트가 레이어 크기로 잘릴 수 있습니다(지정된 경우). <span class="varname"> textPs= </span>에서 지원하는 유일한 <span class="codeph"> resMode </span> 옵션입니다. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> autoRes </span> </p> </td> 
      <td class="stentry"> <p>레이어 rect를 텍스트로 가장 잘 채우도록 해상도를 자동으로 조정합니다. </p> <p>를 사용하여 텍스트 상자가 잘릴 위험 없이 가능한 한 많이 채워지도록 텍스트 크기를 자동으로 조정합니다. 자동 줄 바꿈을 사용하면 최종 해상도에서 텍스트가 다시 줄 바꿈될 수 있습니다. <span class="varname"> autoRes </span>을(를) 선택한 경우 <span class="codeph"> res </span>이(가) 무시됩니다. <span class="codeph"> textPs= </span>에서 지원되지 않습니다. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> maxRes </span> </p> </td> 
      <td class="stentry"> <p>지정된 해상도를 사용합니다. 필요한 경우 텍스트를 레이어 rect로 자르지 않도록 줄이십시오. </p> <p>클리핑이 발생하지 않는 한 지정된 해상도로 텍스트를 렌더링하는 데 사용합니다. 클리핑이 있는 경우 모든 텍스트가 텍스트 상자 내에 완전히 포함되도록 해상도가 자동으로 감소합니다. 자동 줄 바꿈을 사용하면 최종 해상도에서 텍스트가 다시 줄 바꿈될 수 있습니다. <span class="codeph"> textPs= </span>에서 지원되지 않습니다. </p> </td> 
     </tr> 
    </table> </p> <p>텍스트 레이어 크기가 size=로 지정되지 않았거나 너비만 지정된 경우 'autoRes' 및 'maxRes' 설정이 무시됩니다. 이 경우 지정된 해상도를 사용하여 텍스트를 렌더링합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 단어 줄바꿈 </span> </span> </p> </td> 
  <td class="stentry"> <p>줄바꿈 모드를 지정합니다. </p> <p> <span class="codeph"> 줄바꿈 | noRap | nbWrap </span> </p> <p> 
    <table id="simpletable_FF2510E029EC41E29BC30D9FC2923EA3"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 줄 바꿈 </span> </p> </td> 
      <td class="stentry"> <p>자동 줄 바꿈을 비활성화합니다. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 줄 바꿈 </span> </p> </td> 
      <td class="stentry"> <p>표준 자동 줄 바꿈을 활성화합니다. </p> <p>필요하면 긴 말을 가로막는다. <span class="codeph"> textPs= </span>은(는) <span class="codeph"> 줄바꿈 </span>만 지원합니다. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nbWrap </span> </p> </td> 
      <td class="stentry"> <p>단어 잘림 방지 줄바꿈을 활성화합니다. </p> <p>단어 끝부분이 잘려도 단어 하나 깨지지 않습니다. 일반적으로 긴 단어가 손상되지 않도록 하기 위해 <span class="codeph"> autoRes </span> 또는 <span class="codeph"> maxRes </span>과(와) 함께 사용됩니다. </p> </td> 
     </tr> 
    </table> </p> <p><span class="codeph"> 줄 바꿈 </span> 및 <span class="codeph"> 줄 바꿈 </span>은(는) 단어 경계와 하이픈에서 자동 줄 바꿈을 수행합니다. </p> </td> 
 </tr> 
</table>

## 속성 {#section-114ca0b8585b403c873e2251478ad1d5}

텍스트 레이어 속성입니다. 이미지, 단색 및 효과 레이어에서 무시됩니다. `layer=0`에 대해 지정된 경우 `layer=comp`에 적용됩니다.

## 기본값 {#section-855230f5330b4afc8a933f00a1ed4612}

`textAttr=72,norm,fixedRes,wrap`

## 참조 {#section-68b0d2e2d0474e2097a9331ae272c224}

[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) , [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
