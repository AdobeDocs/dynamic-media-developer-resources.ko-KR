---
description: 레이어 텍스트(Adobe Photoshop 호환) 텍스트 레이어의 텍스트 본문을 지정합니다.
seo-description: 레이어 텍스트(Adobe Photoshop 호환) 텍스트 레이어의 텍스트 본문을 지정합니다.
seo-title: textPs
solution: Experience Manager
title: textPs
topic: Scene7 Image Serving - Image Rendering API
uuid: 45e587b6-8dc8-408c-ade6-d70025fd1117
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# textPs{#textps}

레이어 텍스트(Adobe Photoshop 호환) 텍스트 레이어의 텍스트 본문을 지정합니다.

`textPs= *`문자열`*`

<table id="simpletable_4E2D08FD4EEC4EDC9EFE9F6F2E22DB0C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 문자열</span></span> </p> </td> 
  <td class="stentry"> <p>서식 있는 텍스트 형식(RTF) 문자열. </p></td> 
 </tr> 
</table>

모든 글꼴, 글꼴 색상 및 단락 서식 지정 컨트롤은 RTF 명령을 사용하여 가능합니다.

텍스트 [서식을 참조하십시오](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c).

`textPs=` 를 사용하면 맞춤, `textFlowPath=` 및/또는 로 정의된 사각형이 아닌 영역으로 텍스트 흐름, 임의 패스로 텍스트 렌더링 등의 확장 기능을 사용할 수 `textFlowXPath=``textPath=`있습니다.

## 속성 {#section-a289dc26b6534b41998b1e241d5f2f92}

레이어 특성. 해당되는 `layer=0` 경우에 `layer=comp`적용됩니다. 동일한 레이어에서 `src=` 및 `text=` 함께 사용할 수 없습니다. 마지막으로 `text=`나타나는 이미지, `textPs=`및 `src=` 텍스트 레이어인지 여부를 결정합니다. 효과 레이어에서 무시됩니다.

## 기본값 {#section-11c2ae2c96d64a0a9c207252df663e4d}

없음.

## 참조 {#section-5c2b25767d2b47b5be817271ab12e13c}

[텍스트 서식 지정](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowxpath.md#reference-c55d4e41a28f40aca6a24ca218c28542)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd)[, textTextPathFlow=TextFlowFlowTextFlowXpPath=Path, TextPath=Angle, textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15)
