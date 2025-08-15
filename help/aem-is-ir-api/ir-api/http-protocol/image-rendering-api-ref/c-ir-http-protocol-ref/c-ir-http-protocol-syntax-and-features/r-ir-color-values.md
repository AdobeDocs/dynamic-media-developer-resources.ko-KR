---
title: 색상 값
description: color= 및 bgc= 속성에 대한 색상 값은 HTML과 마찬가지로 십진수로 쉼표로 구분된 구성 요소 값 목록 또는 16진수 표기법을 사용하여 지정할 수 있습니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 608ff0f1-4fbd-4e32-af07-3a62569d14c7
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 4%

---

# 색상 값{#color-values}

`color=` 및 `bgc=` 특성에 대한 색상 값은 HTML과 유사한 십진수, 쉼표로 구분된 구성 요소 값 목록 또는 16진수 표기법을 사용하여 지정할 수 있습니다.

<table id="simpletable_9B3A231D5BB14A3DB2B42B341E198341"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 색상</span> </p></td> 
  <td class="stentry"> <p><span class="codeph">{ {red , green , blue} | 회색 } | { [ 0x ] hex6 } | { 0xhex2 }</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>빨강, 녹색, 파랑, 회색</i> </p></td> 
  <td class="stentry"> <p>색상 구성 요소 값(0...255, 10진수) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>hex6</i> </p></td> 
  <td class="stentry"> <p>6자리 16진수 RGB 색상 값(RRGGBB)이 포장되었습니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>hex2</i> </p></td> 
  <td class="stentry"> <p>2자리 16진수 회색 값(0...FF)이 팩에 포함되어 있습니다. </p></td> 
 </tr> 
</table>

## 예제 {#section-a78732151d584e84abeb99f9ce8d7c24}

유효한 색상 지정자 및 해당 RGB 색상 값 해석의 몇 가지 예:

<table id="simpletable_837B3173020240A5B7B2DB2F4CC57352"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,100,200 </p></td> 
  <td class="stentry"> <p>(0,100,200) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>128 </p></td> 
  <td class="stentry"> <p>(128,128,128) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0x010203 </p></td> 
  <td class="stentry"> <p>(1,2,3) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>00b1c2 </p></td> 
  <td class="stentry"> <p>(160,177,194) </p></td> 
 </tr> 
</table>

## 참조 {#section-207d5cb918a94736a27445faa58917d3}

[색상=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa), [bgc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-bgc.md#reference-3f5c78cea01c4a85aa582076d23aebb0), [그룹=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a)
