---
title: 정량화
description: 색상 양자화. GIF 출력 변환을 위한 색상 양자화 속성을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67247016-a038-4ed4-90ed-751eaf9c4881
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---

# 정량화{#quantize}

색상 양자화. GIF 출력 변환을 위한 색상 양자화 속성을 지정합니다.

` quantize= *`type`*[, *`dither`*[, *`numColors`*[, *`colorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 유형 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptive|web|mac} </span> 팔레트 유형 </p> <p>' <span class="codeph"> 웹 </span>' 또는 ' <span class="codeph"> mac </span>'을(를) 선택하여 미리 정의된 팔레트를 선택하거나 ' <span class="codeph"> 적응형 </span>'(으)로 설정하여 이미지에 대한 최적 팔레트를 계산합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 디더 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {diffuse|off} </span> 디더링 옵션 </p> <p>디더링을 비활성화하려면 Floyd-Steinberg 오류 확산에 대해 '확산'을 선택하거나 '해제'를 선택합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
  <td class="stentry"> <p>'<span class="codeph"> 응용 프로그램 </span>' 팔레트에 포함된 출력 색(정수) 수입니다. </p> <p> <span class="codeph"> <span class="varname"> numColors </span> </span>은(는) 2에서 256 사이여야 합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 색 목록 </span> </span> </p> </td> 
  <td class="stentry"> <p>16진수 6 형식의 강제 RGB 색상에 대한 쉼표로 구분된 목록입니다. '<span class="codeph"> 적응형 </span>' 팔레트에 포함할 강제 색상을 지정할 수 있습니다. 지정된 색상 수가 <span class="codeph"> numColors </span>보다 작으면 이미지 내용을 기반으로 추가 색상이 계산됩니다. </p> <p><span class="codeph"> fmt=gif </span> 또는 <span class="codeph"> fmt=gif-alpha </span>인 경우에만 사용됩니다. 그렇지 않으면 무시됩니다. <span class="codeph"> <span class="varname"> colorList </span> </span>(으)로 지정된 색상은 hex6 형식의 RGB 값이어야 합니다(<span class="codeph"> 색 </span> 참조). 다른 색 지정자는 허용되지 않습니다. </p> </td> 
 </tr> 
</table>

## 기본값 {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## 예 {#section-b3a979dc9ae3459baa093bf17310988f}

&#39;`web`&#39; 팔레트를 사용하고 디더링 없이 GIF 축소판을 생성합니다.

[!DNL `http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`]

이미지를 키 색상 투명도를 갖는 두 색조 GIF으로 변환하고 색상을 검정과 흰색으로 강제 변환합니다.

[!DNL `http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`]
