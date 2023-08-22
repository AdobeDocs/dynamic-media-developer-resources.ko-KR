---
title: 텍스트 흐름 경로
description: 텍스트 흐름 영역. textPs=로 지정된 텍스트가 유입되는 영역을 하나 이상 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b5575d17-150b-421c-b298-077b577eb95c
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 2%

---

# 텍스트 흐름 경로{#textflowpath}

텍스트 흐름 영역. textPs=로 지정된 텍스트가 유입되는 영역을 하나 이상 지정합니다.

` textFlowPath= *`pathDefinition`*`

<table id="simpletable_52CEFF5C3CCB4642A9A320D01B1BF8E0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pathDefinition </span> </p> </td> 
  <td class="stentry"> <p>경로 데이터. </p> </td> 
 </tr> 
</table>

다음을 참조하십시오 [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) 추가 정보: 설명 포함 *`pathDefinition`*.

RTF 여백 명령 `\margl`, `\margr`, `\margt`, 및 `\margb` 다음의 경우 무시됨 `textFlowPath=` 이(가) 있습니다. 경로 정의를 지정하지 않은 경우 `textFlowPath=` 은(는) 무시됩니다.

## 속성 {#section-b68dc887c6534ce8982cad740b3aeaa4}

텍스트 레이어 속성( `textPs=` 만 해당). 다른 레이어에서 무시됨. 적용 대상 `layer=0` 에 대해 지정된 경우 `layer=comp`.

## 기본값 {#section-68c4559b9e8242059b82e5a39a455dfc}

레이어 사각형과 같습니다. 텍스트는 전체 레이어 사각형을 채웁니다.

## 참조 {#section-592b0039cf99471188db6a7df44b450a}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) , [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), [textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15), [텍스트 레이어](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
