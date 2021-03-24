---
description: 레이어 색상을 참조하십시오. 단색 및 효과 레이어의 전경색과 불투명도, 텍스트 레이어의 텍스트 상자 채우기 색상을 지정합니다.
solution: Experience Manager
title: color
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 3%

---


# color{#color}

레이어 색상을 참조하십시오. 단색 및 효과 레이어의 전경색과 불투명도, 텍스트 레이어의 텍스트 상자 채우기 색상을 지정합니다.

` color= *`color`*`

<table id="simpletable_68645167998A42229CEF858909FD447E"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> color  </span> </span> </p> </td> 
  <td class="stentry"> <p>알파 포함 또는 알파 없는 회색, RGB 또는 CMYK 색상 값 </p> </td> 
 </tr> 
</table>

이미지 및 텍스트 레이어의 경우 `color=`은 `rotate=` 및 `extend=`가 적용되기 전에 지정된 색상*으로 레이어의 테두리 사각형 내의 투명 및 반불투명 영역을 칠합니다.

## 속성 {#section-d6e74c36a49547849212e4db8927e678}

레이어 속성입니다. 현재 레이어나 `layer=comp`인 경우 레이어 0에 적용됩니다.

*`color`* 의 픽셀 유형에 해당하는 작업 색상 공간에 존재하는 것으로 가정합니다 *`color`*. *`color`* 레이어 이미지에 병합 시 다른 픽셀 유형이 있는 경우 가 정확하게 변환됩니다.

## 기본값 {#section-60611c72876b4c45b5c85ce35608e5ec}

단색 및 효과 레이어의 기본값은 없습니다.색상을 지정해야 합니다. 이미지 및 텍스트 레이어의 기본값은 0,0,0,0(완전 투명)입니다.

## 예 {#section-2d090493f4ec4e188bbc5565aa151a05}

다음 템플릿 조각에서 텍스트 배경을 50% 불투명 색상으로 설정하고 동일한 색상을 사용하여 레이어 2 이미지 주위에 반투명 10픽셀 테두리를 추가합니다.

`…&$color=214,245,130,128& layer=1&text=my-text-string&color=$color$&… layer=2&src=myRootId/myImageId&extend=10,10,10,10&bgColor=$color$&…`

## 참조 {#section-f0e059f857b64b61ab4f23312b8dc619}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93),  [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab),  [opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5),  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)  [bgc=, 색상 관리](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
