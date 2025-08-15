---
title: textPs
description: 레이어 텍스트(Adobe Photoshop 호환). 텍스트 레이어의 텍스트 본문을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 95f343ce-bea3-425e-9a25-d1d141a976d9
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 3%

---

# textPs{#textps}

레이어 텍스트(Adobe Photoshop 호환). 텍스트 레이어의 텍스트 본문을 지정합니다.

`textPs= *`문자열`*`

<table id="simpletable_4E2D08FD4EEC4EDC9EFE9F6F2E22DB0C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 문자열</span> </span> </p> </td> 
  <td class="stentry"> <p>서식 있는 텍스트(RTF) 문자열입니다. </p></td> 
 </tr> 
</table>

모든 글꼴, 글꼴 색상 및 단락 서식 제어는 RTF 명령을 사용하여 수행됩니다.

[텍스트 서식](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c)을 참조하세요.

`textPs=`은(는) 양쪽 맞춤, `textFlowPath=` 및/또는 `textFlowXPath=`(으)로 정의된 사각형이 아닌 영역으로 텍스트 흐름, `textPath=`(으)로 정의된 임의의 경로를 따라 텍스트 렌더링 등 확장된 기능을 지원합니다.

## 속성 {#section-a289dc26b6534b41998b1e241d5f2f92}

레이어 속성입니다. `layer=0`인 경우 `layer=comp`에 적용됩니다. 같은 계층에서 `src=` 및 `text=`과(와) 함께 사용할 수 없습니다. `text=`, `textPs=` 및 `src=`의 마지막 항목이 우세하여 이 항목이 이미지인지 텍스트 레이어인지를 확인합니다. 효과 레이어에서 무시됨.

## 기본값 {#section-11c2ae2c96d64a0a9c207252df663e4d}

없음.

## 참조 {#section-5c2b25767d2b47b5be817271ab12e13c}

[텍스트 서식](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [텍스트=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), [textFlowXPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowxpath.md#reference-c55d4e41a28f40aca6a24ca218c28542), [textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd), [textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15)
