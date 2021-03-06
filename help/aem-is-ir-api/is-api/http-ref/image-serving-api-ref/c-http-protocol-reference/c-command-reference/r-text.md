---
description: 레이어 텍스트. 텍스트 레이어의 텍스트와 서식을 지정합니다.
solution: Experience Manager
title: 텍스트
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3966b180-bef1-4fad-af71-ba42bbdffd59
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 5%

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

모든 글꼴, 글꼴 색상 및 단락 서식 컨트롤은 RTF 명령을 사용하여 수행합니다. 자세한 내용은 [텍스트 서식](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c)을 참조하십시오.

`text=` 에서는 텍스트 자동 크기 조절을 사용하여 지정된 레이어 사각형을 채울 수  `size=`있습니다.

[textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)을 참조하십시오.

`text=` 에서는 렌더링된 텍스트에 맞게 텍스트 레이어의 자동 크기 조정을 지원합니다( `size=` 가 지정되지 않았거나 너비만 지정된 경우). 이 경우 RTF 정렬 명령 `\ql`, `\qr` 및 `\qc` 중 하나만 적용될 수 있습니다. 그렇지 않으면 오류가 반환됩니다.

## 속성 {#section-8c0f020094a44c6b858454ef91ab4edf}

레이어 속성입니다. `layer=comp`인 경우 `layer=0`에 적용됩니다. 동일한 계층에서 `src=` 및 `textPs=`과 함께 사용할 수 없습니다. `text=`, `textPs=` 및 `src=`의 마지막 발생 항목을 정의하고 이 항목이 이미지인지 텍스트 레이어인지 확인합니다. 효과 레이어에서 무시됨.

## 기본값 {#section-58958671e0ad479e8d5f6c1d41d7dc74}

없음.

## 예 {#section-d011f765ec5c418d814a821019b0eef0}

[템플릿](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)의 [텍스트 형식](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) 및 [예제 A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac)에서 예제를 참조하십시오.

## 참조 {#section-207b779ab67342a5acd343e6bcc749c4}

[텍스트 서식](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c),  [텍스트 위치 지정](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87),  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d),  [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
