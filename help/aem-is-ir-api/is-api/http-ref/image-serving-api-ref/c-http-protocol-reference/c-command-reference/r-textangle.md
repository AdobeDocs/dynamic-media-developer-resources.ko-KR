---
title: 텍스트 각도
description: 텍스트 렌더링 방향. textPs=로 지정된 텍스트를 정렬하여 텍스트 상자(size= 또는 textFlowPath=로 정의됨)에 렌더링하는 각도를 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 102dbdc0-77b8-4c60-b456-6cf693e0b38b
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 2%

---

# 텍스트 각도{#textangle}

텍스트 렌더링 방향. textPs=로 지정된 텍스트를 정렬하여 텍스트 상자(size= 또는 textFlowPath=로 정의됨)에 렌더링하는 각도를 지정합니다.

` textAngle= *`각도`*`

<table id="simpletable_40832AC4B43A458CA69B225768124F58"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 각도 </span> </p> </td> 
  <td class="stentry"> <p>방향 각도(도)입니다. </p> </td> 
 </tr> 
</table>

양수 값은 텍스트를 시계 방향으로 회전합니다. `textAngle=90`은(는) 텍스트를 위에서 아래로 그립니다.

## 속성 {#section-6d586a632daa4261a8ce62db56140b36}

레이어 속성입니다. `layer=comp`인 경우 `layer=0`에 적용됩니다. 이 레이어에 `textPs=`이(가) 지정되지 않았거나 `textPath=`이(가) 지정된 경우 무시됩니다.

## 기본값 {#section-49a9f5819c994c27928282c14b2bb2a7}

순환이 없는 경우 `textAngle=0`.

## 참조 {#section-dccc29ff33704061b2519b56b7be45fd}

[텍스트 서식](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c), [텍스트 위치](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87), [텍스트 흐름=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [텍스트 흐름 경로=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), [텍스트 경로=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd)
