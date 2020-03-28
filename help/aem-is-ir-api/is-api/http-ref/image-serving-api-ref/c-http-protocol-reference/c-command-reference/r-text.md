---
description: 레이어 텍스트. 텍스트 레이어의 텍스트와 서식을 지정합니다.
seo-description: 레이어 텍스트. 텍스트 레이어의 텍스트와 서식을 지정합니다.
seo-title: 텍스트
solution: Experience Manager
title: 텍스트
topic: Scene7 Image Serving - Image Rendering API
uuid: 5b4f9282-83a3-488d-b5d2-deb2c92de564
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 텍스트{#text}

레이어 텍스트. 텍스트 레이어의 텍스트와 서식을 지정합니다.

` text= *`문자열`*`

<table id="simpletable_6C095D7F69874A8EA3D1D52103FA520C"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 문자열 </span> </p> </td> 
  <td class="stentry"> <p>서식 있는 텍스트 형식(RTF) 문자열 또는 일반 텍스트 문자열입니다. </p> </td> 
 </tr> 
</table>

모든 글꼴, 글꼴 색상 및 단락 서식 지정 컨트롤은 RTF 명령을 사용하여 가능합니다. 자세한 내용은 [텍스트](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) 서식 지정을 참조하십시오.

`text=` 에서는 텍스트 자동 크기 조정을 통해 지정된 레이어 사각형을 채울 수 `size=`있습니다.

textAttr= [을 참조하십시오](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d).

`text=` 에서는 렌더링된 텍스트에 맞게 텍스트 레이어의 자동 크기 조정을 지원합니다( `size=` 지정하지 않았거나 너비만 지정된 경우). 이 경우 RTF 정렬 명령 중 하나만 `\ql`적용되며 `\qr`적용될 `\qc` 수 있습니다.그렇지 않으면 오류가 반환됩니다.

## 속성 {#section-8c0f020094a44c6b858454ef91ab4edf}

레이어 특성. 해당되는 `layer=0` 경우에 `layer=comp`적용됩니다. 동일한 레이어와 함께 `src=` 및 `textPs=` 함께 사용할 수 없습니다.마지막으로 나타나는 `text=`이미지 `textPs=`및 `src=` 텍스트 레이어인지 여부를 확인하고 정의할 수 있습니다. 효과 레이어에서 무시됩니다.

## 기본값 {#section-58958671e0ad479e8d5f6c1d41d7dc74}

없음.

## 예 {#section-d011f765ec5c418d814a821019b0eef0}

텍스트 서식 지정 및 [템플릿의](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) 예제 [A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) 에 있는 예제를 [참조하십시오](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## 참조 {#section-207b779ab67342a5acd343e6bcc749c4}

[텍스트 서식 지정](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c), [텍스트](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87)위치 [지정](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [textAttr=, textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
