---
title: clipXPath
description: 반전된 레이어 클립 경로입니다. 현재 레이어의 제외 클립 경로를 지정합니다. clipXPath=로 정의된 영역 내에 있는 레이어의 모든 부분이 투명하게 렌더링됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7d7e92f5-856f-4d62-a5d3-4726d7b43792
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 3%

---

# clipXPath{#clipxpath}

반전된 레이어 클립 경로입니다. 현재 레이어의 제외 클립 경로를 지정합니다. clipXPath=로 정의된 영역 내에 있는 레이어의 모든 부분이 투명하게 렌더링됩니다.

`clipXPath= *`pathDefinition`*`

`clipXPathE= *`pathName`*&#42;[, *`pathName`*]`

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

다음을 참조하십시오 [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) 추가 정보: 설명 포함 `*`pathName`*` 및 `*`pathDefinition`*`.

## 속성 {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

레이어 속성입니다. 다음과 같은 경우 현재 레이어 또는 합성 이미지에 적용됩니다. `layer=comp`. 다음과 같은 경우 무시됨 `clipPath=` 이(가) 지정되지 않았습니다. 효과 레이어에서 무시됨.

## 기본값 {#section-d1986aa31af14767aeb1b4a57add67f4}

없음.

## 참조 {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
