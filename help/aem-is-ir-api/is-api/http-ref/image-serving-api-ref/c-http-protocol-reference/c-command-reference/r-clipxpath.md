---
description: 반전된 레이어 클립 경로. 현재 레이어의 제외 클립 경로를 지정합니다. clipXPath=로 정의된 영역 내에 있는 레이어의 모든 부분은 투명하게 렌더링됩니다.
solution: Experience Manager
title: clipXPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7d7e92f5-856f-4d62-a5d3-4726d7b43792
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 4%

---

# clipXPath{#clipxpath}

반전된 레이어 클립 경로. 현재 레이어의 제외 클립 경로를 지정합니다. clipXPath=로 정의된 영역 내에 있는 레이어의 모든 부분은 투명하게 렌더링됩니다.

`clipXPath= *`pathDefinition`*`

`clipXPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="simpletable_27AFC3A694874CF8B673460820EFD90D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>경로 데이터. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span> </span> </p> </td> 
  <td class="stentry"> <p>레이어 소스 이미지에 포함된 경로 이름(ASCII만 해당). </p></td> 
 </tr> 
</table>

`*`pathName`*` 및 `*`pathDefinition`*`에 대한 설명을 포함하여 추가 정보는 [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)을 참조하십시오.

## 속성 {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

레이어 속성입니다. `layer=comp` 인 경우 현재 레이어 또는 복합 이미지에 적용됩니다. `clipPath=`이 지정되지 않은 경우 무시됩니다. 효과 레이어에서 무시됨.

## 기본값 {#section-d1986aa31af14767aeb1b4a57add67f4}

없음.

## 참조 {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
