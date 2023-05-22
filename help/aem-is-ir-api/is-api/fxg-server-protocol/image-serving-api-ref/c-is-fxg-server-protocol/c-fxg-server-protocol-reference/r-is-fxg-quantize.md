---
description: 색상 양자화. GIF 출력 변환을 위한 색상 양자화 속성을 지정합니다.
solution: Experience Manager
title: 정량화
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67247016-a038-4ed4-90ed-751eaf9c4881
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 1%

---

# 정량화{#quantize}

색상 양자화. GIF 출력 변환을 위한 색상 양자화 속성을 지정합니다.

` quantize= *`유형`*[, *`디더`*[, *`numColors`*[, *`색상 목록`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 유형 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptive|web|mac} </span> 팔레트 유형 </p> <p>선택 ' <span class="codeph"> 웹 </span>' 또는 ' <span class="codeph"> mac </span>' 사전 정의된 팔레트를 선택하거나 ' <span class="codeph"> 자동 선택 </span>이미지에 대한 최적 팔레트를 계산합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 디더 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {diffuse|off} </span> 디더링 옵션 </p> <p>디더링을 비활성화하려면 Floyd-Steinberg 오류 확산에 대해 '확산'을 선택하거나 '해제'를 선택합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
  <td class="stentry"> <p>""에 포함된 출력 색상 수(정수) <span class="codeph"> 자동 선택 </span>' 팔레트. </p> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> 은(는) 2~256 사이여야 합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 색상 목록 </span> </span> </p> </td> 
  <td class="stentry"> <p>16진수6 포맷으로 쉼표로 구분된 강제 RGB 색상 목록입니다. 에 포함할 강제 색상을 지정할 수 있습니다. <span class="codeph"> 자동 선택 </span>' 팔레트. 지정한 색상 수가 보다 작은 경우 <span class="codeph"> numColors </span>, 추가 색상은 이미지 콘텐츠를 기반으로 계산됩니다. </p> <p>다음과 같은 경우에만 사용됨 <span class="codeph"> fmt=gif </span> 또는 <span class="codeph"> fmt=gif-alpha </span>. 그렇지 않으면 무시됩니다. 에 지정된 색상 <span class="codeph"> <span class="varname"> 색상 목록 </span> </span> 은(는) 16진수 6 형식의 RGB 값이어야 합니다(참조). <span class="codeph"> 색상 </span>); 다른 색상 지정자는 허용되지 않습니다. </p> </td> 
 </tr> 
</table>

## 기본값 {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## 예 {#section-b3a979dc9ae3459baa093bf17310988f}

를 사용하여 GIF 썸네일 생성 `web`&#39; 팔레트 및 디더링 없음:

[!DNL http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off]

이미지를 키 색상 투명도를 사용하는 두 가지 색상 GIF으로 변환하고 색상을 검정과 흰색으로 강제 변환합니다.

[!DNL http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff]
