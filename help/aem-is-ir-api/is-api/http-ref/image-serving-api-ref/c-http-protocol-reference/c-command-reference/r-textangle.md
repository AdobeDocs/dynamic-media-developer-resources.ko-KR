---
description: 텍스트 렌더링 방향 textPs=로 지정된 텍스트를 배치하고 텍스트 상자에 렌더링할 각도를 지정합니다(size= 또는 textFlowPath=).
seo-description: 텍스트 렌더링 방향 textPs=로 지정된 텍스트를 배치하고 텍스트 상자에 렌더링할 각도를 지정합니다(size= 또는 textFlowPath=).
seo-title: textAngle
solution: Experience Manager
title: textAngle
topic: Scene7 Image Serving - Image Rendering API
uuid: ac54c186-1fc5-479a-89f2-ff2da5e7999a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 4%

---


# textAngle{#textangle}

텍스트 렌더링 방향 textPs=로 지정된 텍스트를 배치하고 텍스트 상자에 렌더링할 각도를 지정합니다(size= 또는 textFlowPath=).

` textAngle= *`각도`*`

<table id="simpletable_40832AC4B43A458CA69B225768124F58"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 각도 </span> </p> </td> 
  <td class="stentry"> <p>방향 각도(도). </p> </td> 
 </tr> 
</table>

양수 값은 텍스트를 시계 방향으로 회전합니다.`textAngle=90`은 텍스트를 위쪽에서 아래쪽으로 그립니다.

## 속성 {#section-6d586a632daa4261a8ce62db56140b36}

레이어 속성입니다. `layer=comp`인 경우 `layer=0`에 적용됩니다. 이 레이어에 대해 `textPs=`이(가) 지정되지 않았거나 `textPath=`이(가) 지정된 경우 무시됩니다.

## 기본값 {#section-49a9f5819c994c27928282c14b2bb2a7}

`textAngle=0` 을 클릭합니다.

## 참조 {#section-dccc29ff33704061b2519b56b7be45fd}

[텍스트 서식](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c),  [텍스트 위치 지정](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87),  [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)  [, textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd)
