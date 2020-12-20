---
description: 텍스트 흐름 영역. textPs=로 지정된 텍스트를 흐리게 할 영역을 하나 이상 지정합니다.
seo-description: 텍스트 흐름 영역. textPs=로 지정된 텍스트를 흐리게 할 영역을 하나 이상 지정합니다.
seo-title: textFlowPath
solution: Experience Manager
title: textFlowPath
topic: Scene7 Image Serving - Image Rendering API
uuid: 5449d78f-e56b-4afb-a05a-7cf8f1f37278
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 3%

---


# textFlowPath{#textflowpath}

텍스트 흐름 영역. textPs=로 지정된 텍스트를 흐리게 할 영역을 하나 이상 지정합니다.

` textFlowPath= *`pathDefinition`*`

<table id="simpletable_52CEFF5C3CCB4642A9A320D01B1BF8E0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pathDefinition  </span> </p> </td> 
  <td class="stentry"> <p>경로 데이터. </p> </td> 
 </tr> 
</table>

*`pathDefinition`*&#x200B;에 대한 설명을 비롯한 자세한 내용은 [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)을 참조하십시오.

`textFlowPath=`이(가) 있는 경우 RTF 여백 명령 `\margl`, `\margr`, `\margt` 및 `\margb`은 무시됩니다. 경로 정의를 지정하지 않으면 `textFlowPath=`은 무시됩니다.

## 속성 {#section-b68dc887c6534ce8982cad740b3aeaa4}

텍스트 레이어 특성( `textPs=`만 해당). 다른 레이어에서 무시됩니다. `layer=comp`에 대해 지정된 경우 `layer=0`에 적용됩니다.

## 기본값 {#section-68c4559b9e8242059b82e5a39a455dfc}

레이어 사각형과 동일;텍스트가 전체 레이어 사각형을 채웁니다.

## 참조 {#section-592b0039cf99471188db6a7df44b450a}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) ,  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef),  [textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15)  [, 텍스트 레이어](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
