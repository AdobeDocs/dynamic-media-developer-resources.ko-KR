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
ht-degree: 4%

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

다음을 참조하십시오 [텍스트 서식](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c).

`textPs=` 는 로 정의된 사각형이 아닌 영역으로 텍스트를 이동하는 자리맞춤과 같은 확장된 기능을 지원합니다. `textFlowPath=` 및/또는 `textFlowXPath=`, 및 로 정의된 임의의 경로를 따른 텍스트 렌더링 `textPath=`.

## 속성 {#section-a289dc26b6534b41998b1e241d5f2f92}

레이어 속성입니다. 적용 대상 `layer=0` if `layer=comp`. 와 상호 배타적 `src=` 및 `text=` 같은 레이어에 있을 수 있습니다. 의 마지막 발생 횟수 `text=`, `textPs=`, 및 `src=` 이 레이어를 우선하여 이미지 레이어인지 텍스트 레이어인지를 결정합니다. 효과 레이어에서 무시됨.

## 기본값 {#section-11c2ae2c96d64a0a9c207252df663e4d}

없음.

## 참조 {#section-5c2b25767d2b47b5be817271ab12e13c}

[텍스트 서식](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), [textFlowXPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowxpath.md#reference-c55d4e41a28f40aca6a24ca218c28542), [textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd), [textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15)
