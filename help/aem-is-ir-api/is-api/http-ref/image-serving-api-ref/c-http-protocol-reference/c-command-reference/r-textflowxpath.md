---
description: 텍스트 흐름 제외 영역. 텍스트 흐름에서 제외할 하나 이상의 영역을 지정합니다.
seo-description: 텍스트 흐름 제외 영역. 텍스트 흐름에서 제외할 하나 이상의 영역을 지정합니다.
seo-title: textFlowXPath
solution: Experience Manager
title: textFlowXPath
topic: Scene7 Image Serving - Image Rendering API
uuid: ce833ae7-e774-4954-a521-b6247e75f6eb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 5%

---


# textFlowXPath{#textflowxpath}

텍스트 흐름 제외 영역. 텍스트 흐름에서 제외할 하나 이상의 영역을 지정합니다.

`textFlowXPath= *`pathDefinition`*`

<table id="simpletable_7E0EA48AEBB5426CBE948FCA18882C66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>경로 데이터. </p></td> 
 </tr> 
</table>

*`pathDefinition`*&#x200B;에 대한 설명을 비롯한 자세한 내용은 [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)을 참조하십시오. 경로 정의를 지정하지 않으면 `textFlowXPath=`은 무시됩니다.

## 속성 {#section-cd1ebb151d4a405fbfc508d46522d686}

텍스트 레이어 특성( `textPs=`만 해당). 다른 레이어에서 무시하거나 `textFlowPath=` 없이 지정할 때 무시됩니다. `layer=comp`에 대해 지정된 경우 `layer=0`에 적용됩니다.

## 기본값 {#section-9405cda904684d829ed12a9e40a4dc46}

없음.

## 참조 {#section-855228e744c7437a921d5db5b24bcd95}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) ,  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)
