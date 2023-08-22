---
title: textFlowXPath
description: 텍스트 흐름 제외 영역. 텍스트 흐름에서 제외할 영역을 하나 이상 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2430ab43-c032-4c2f-93c3-225e8116f100
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 5%

---

# textFlowXPath{#textflowxpath}

텍스트 흐름 제외 영역. 텍스트 흐름에서 제외할 영역을 하나 이상 지정합니다.

`textFlowXPath= *`pathDefinition`*`

<table id="simpletable_7E0EA48AEBB5426CBE948FCA18882C66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>경로 데이터. </p></td> 
 </tr> 
</table>

다음을 참조하십시오 [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) 추가 정보: 설명 포함 *`pathDefinition`*. 경로 정의를 지정하지 않은 경우 `textFlowXPath=` 은(는) 무시됩니다.

## 속성 {#section-cd1ebb151d4a405fbfc508d46522d686}

텍스트 레이어 속성( `textPs=` 만 해당). 다른 레이어에서 무시되거나 `textFlowPath=`. 적용 대상 `layer=0` 에 대해 지정된 경우 `layer=comp`.

## 기본값 {#section-9405cda904684d829ed12a9e40a4dc46}

없음.

## 참조 {#section-855228e744c7437a921d5db5b24bcd95}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) , [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)
