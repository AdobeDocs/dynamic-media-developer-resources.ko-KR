---
description: 텍스트 레이어 속성입니다. rtf 명령으로 사용할 수 없는 텍스트 레이어의 추가 특성을 지정합니다.
solution: Experience Manager
title: textAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 0c8a3d2a-2524-436a-8bc7-60241af0fd17
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 1%

---

# textAttr{#textattr}

텍스트 레이어 속성입니다. rtf 명령으로 사용할 수 없는 텍스트 레이어의 추가 특성을 지정합니다.

` textAttr= *``*[, *``*[, *``*[, *`resantiAliasingresModewordWrap`*]]]`

<table id="simpletable_0072BF7DF52B4959A14EDEF60A6EBDEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> res  </span> </span> </p> </td> 
  <td class="stentry"> <p>글꼴 크기를 변경하지 않고 텍스트 레이어의 크기를 조정하는 수단을 제공합니다. 해상도 값이 높을수록 캔버스 크기에 비해 렌더링된 텍스트의 크기가 커집니다.값이 작을수록 텍스트 크기가 줄어듭니다. 인치당 점(0보다 큼)의 텍스트 해상도. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 앤티앨리어싱  </span> </span> </p> </td> 
  <td class="stentry"> <p>텍스트 렌더링 엔진에 적용되는 앤티앨리어싱 모드를 제어합니다. </p> <p> <span class="codeph"> 해제 | 기준 | 바삭하 | 날카로운 | 강함 | 평활  </span> </p> <p> 
    <table id="simpletable_AE2331118FCA4BC7877233E287CED6A4"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 꺼짐 </span> </p> </td> 
      <td class="stentry"> <p>텍스트 앤티앨리어싱을 비활성화합니다. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 규범  </span> </p> </td> 
      <td class="stentry"> <p>표준 텍스트 앤티앨리어싱 모드(기본값)를 활성화합니다. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 파삭파삭해  </span> </p> </td> 
      <td class="stentry"> <p>Photoshop 앤티앨리어싱 모드 <span class="codeph"> 바삭한 </span>( <span class="codeph"> textPs= </span>만 해당)를 선택합니다. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 날카로운  </span> </p> </td> 
      <td class="stentry"> <p>Photoshop 앤티앨리어싱 모드 <span class="codeph"> sharp </span>( <span class="codeph"> textPs= </span>만 해당)를 선택합니다. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 강력함 </span> </p> </td> 
      <td class="stentry"> <p>Photoshop 앤티앨리어싱 모드 <span class="codeph"> strong </span>( <span class="codeph"> textPs= </span>만 해당)을 선택합니다. </p> </td> 
     </tr> 
    </table> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> resMode </span> </span> </p> </td> 
  <td class="stentry"> <p>텍스트를 렌더링할 때 사용된 모양을 제어합니다 </p> <p> <span class="codeph"> fixedRes | autoRes | maxRes  </span> </p> <p> 
    <table id="simpletable_2CFC06DB37154C7C92614FDF7A818DB5"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> fixedRes  </span> </p> </td> 
      <td class="stentry"> <p>지정된 해상도를 사용합니다. </p> <p>텍스트를 합성 캔버스에 대해 정확한 크기로 렌더링하려는 경우 사용합니다. 텍스트 상자가 너무 작은 경우 텍스트가 레이어 크기(지정된 경우)로 잘릴 수 있습니다. 이는 <span class="codeph"> textPs= </span>에서 지원하는 유일한 <span class="varname"> resMode </span> 옵션입니다. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> autoRes  </span> </p> </td> 
      <td class="stentry"> <p>레이어 레코드를 텍스트로 가장 잘 채우도록 해상도를 자동으로 조정합니다. </p> <p>텍스트 상자가 잘릴 위험이 없이 가능한 한 많이 채워지도록 텍스트 크기를 자동으로 조정하는 데 사용합니다. 자동 줄바꿈을 사용하도록 설정하면 최종 해상도로 텍스트를 다시 래핑할 수 있습니다. <span class="varname"> autoRes </span> 를 선택하면  <span class="codeph"> res </span> 가 무시됩니다. <span class="codeph"> textPs= </span>에서 지원되지 않습니다. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> maxRes  </span> </p> </td> 
      <td class="stentry"> <p>지정된 해상도를 사용합니다.텍스트가 레이어 요약으로 잘리지 않도록 하려면 필요한 경우 줄입니다. </p> <p>클리핑이 발생하지 않는 한 지정된 해상도로 텍스트를 렌더링하는 데 사용합니다. 클리핑의 경우 해상도가 자동으로 감소하여 모든 텍스트가 텍스트 상자 내에 완전히 포함되도록 합니다. 자동 줄바꿈을 사용하도록 설정하면 최종 해상도로 텍스트를 다시 래핑할 수 있습니다. <span class="codeph"> textPs= </span>에서 지원되지 않습니다. </p> </td> 
     </tr> 
    </table> </p> <p>텍스트 레이어 크기를 size=로 지정하지 않거나 너비만 지정하면 'autoRes' 및 'maxRes' 설정이 무시되고 지정된 해상도를 사용하여 텍스트를 렌더링합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> wordWrap  </span> </span> </p> </td> 
  <td class="stentry"> <p>래핑 모드를 지정합니다. </p> <p> <span class="codeph"> 랩 | noWrap | nbWrap  </span> </p> <p> 
    <table id="simpletable_FF2510E029EC41E29BC30D9FC2923EA3"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> noWrap  </span> </p> </td> 
      <td class="stentry"> <p>자동 줄바꿈을 비활성화합니다. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 줄바꿈 </span> </p> </td> 
      <td class="stentry"> <p>표준 자동 줄 바꿈을 활성화합니다. </p> <p>필요한 경우 긴 단어를 구분합니다. <span class="codeph"> textPs= </span> 는 줄바꿈만  <span class="codeph"> 지원합니다 </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nbWrap  </span> </p> </td> 
      <td class="stentry"> <p>줄바꿈하지 않는 줄 바꿈을 활성화합니다. </p> <p>마지막에 잘리더라도 단어를 깨지 마십시오. 일반적으로 긴 단어가 끊어지지 않도록 하기 위해 <span class="codeph"> autoRes </span> 또는 <span class="codeph"> maxRes </span>와 함께 사용됩니다. </p> </td> 
     </tr> 
    </table> </p> <p><span class="codeph"> 줄바꿈 </span> 및 <span class="codeph"> 줄바꿈 </span> 단어 경계와 하이픈을 모두 자동 래핑합니다. </p> </td> 
 </tr> 
</table>

## 속성 {#section-114ca0b8585b403c873e2251478ad1d5}

텍스트 레이어 속성입니다. 이미지, 단색 및 효과 레이어에서 무시됩니다. `layer=comp`에 대해 지정된 경우 `layer=0`에 적용됩니다.

## 기본값 {#section-855230f5330b4afc8a933f00a1ed4612}

`textAttr=72,norm,fixedRes,wrap`

## 참조 {#section-68b0d2e2d0474e2097a9331ae272c224}

[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) ,  [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767),  [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
