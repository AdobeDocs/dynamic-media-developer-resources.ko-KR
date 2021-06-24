---
description: 색상 양자화. GIF 출력 변환의 색상 양자화 특성을 지정합니다.
solution: Experience Manager
title: 수량
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 67247016-a038-4ed4-90ed-751eaf9c4881
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 1%

---

# 수량{#quantize}

색상 양자화. GIF 출력 변환의 색상 양자화 특성을 지정합니다.

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorcolorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 유형  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptive|web|mac}  </span> 팔레트 유형 </p> <p>사전 정의된 팔레트를 선택하려면 ' <span class="codeph"> web </span>' 또는 ' <span class="codeph"> mac </span>'를 선택하거나, ' <span class="codeph"> adaptive </span>'로 설정하여 이미지에 대한 최적 팔레트를 계산하십시오. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> dither  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {diffuse|off} 디더링  </span> 옵션 </p> <p>Floyd-Steinberg 오류 확산에는 '확산'을 선택하고 디더링을 비활성화하려면 '해제'를 선택합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> </p> </td> 
  <td class="stentry"> <p>' <span class="codeph"> 적응형 </span>' 팔레트에 포함된 출력 색상(정수)의 수입니다. </p> <p> <span class="codeph"> <span class="varname"> numColors는 2에서 256 사이여야  </span> </span> 합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList  </span> </span> </p> </td> 
  <td class="stentry"> <p>16진수6 형식의 강제 RGB 색상의 쉼표로 구분된 목록입니다. ' <span class="codeph"> 적응형 </span>' 팔레트에 포함할 강제 색상을 지정할 수 있습니다. 지정한 색상 수가 <span class="codeph"> numColors </span>보다 작으면 이미지 내용에 따라 추가 색상이 계산됩니다. </p> <p><span class="codeph"> fmt=gif </span> 또는 <span class="codeph"> fmt=gif-alpha </span>인 경우에만 사용됩니다. 그렇지 않으면 무시됩니다. <span class="codeph"> <span class="varname"> colorList </span> </span>에 지정된 색상은 16진수6 형식의 RGB 값이어야 합니다( <span class="codeph"> color </span> 참조).다른 색상 지정자는 허용되지 않습니다. </p> </td> 
 </tr> 
</table>

## 기본값 {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## 예 {#section-b3a979dc9ae3459baa093bf17310988f}

&#39; `web`&#39; 팔레트를 사용하여 GIF 축소판을 생성하고 디더링을 수행하지 않습니다.

[!DNL http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off]

키 색상 투명도와 힘 색상을 흑백으로 사용하여 이미지를 두 가지 색조 GIF로 변환합니다.

[!DNL http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff]
