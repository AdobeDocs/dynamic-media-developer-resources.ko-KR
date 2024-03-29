---
title: 텍스트 경로
description: 텍스트 경로. textPs=와 함께 제공된 텍스트의 기준선으로 사용할 경로를 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1c515786-bbba-44d3-837e-b474af293b7e
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---

# 텍스트 경로{#textpath}

텍스트 경로. textPs=와 함께 제공된 텍스트의 기준선으로 사용할 경로를 지정합니다.

textPath= *`pathDefinition`*

<table id="simpletable_74F549E8625B483A9B334B24A7EB6D22"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>경로 데이터. </p></td> 
 </tr> 
</table>

다음을 참조하십시오 [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) 추가 정보: 설명 포함 *`pathDefinition`*.

>[!NOTE]
>
>다음과 다름 `clipPath=`하위 경로 끝에 &#39;z&#39; 또는 &#39;Z&#39;를 지정하지 않으면 텍스트 경로가 자동으로 닫히지 않습니다.

*`pathDefinition`* 여러 개의 하위 경로를 포함할 수 있습니다. 텍스트는 지정된 순서대로 하위 경로에 렌더링됩니다.

RTF 명령 `\ql`, `\qc`, `\qr`, `\li`, 및 `\ri` 를 사용하여 렌더링된 텍스트를 패스를 따라 배치할 수 있습니다.

## 속성 {#section-068137df436c46b9b55d271eb60e7285}

텍스트 레이어 속성( `textPs=` 만 해당). 다른 레이어에서 무시됨. 적용 대상 `layer=0` 에 대해 지정된 경우 `layer=comp`. 다음과 같은 경우 무시됨 `textPs=` 있음.

레이어에 두 항목이 모두 포함된 경우 오류가 반환됩니다 `textPath=` 및 `textFlowPath=`.

## 기본값 {#section-697b1f2cfc43498080a31327e6eb173d}

없음, 표준 텍스트 렌더링의 경우.

## 참조 {#section-3050d8f47e1d4f5c9b474dece45ea93d}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) , [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), [텍스트 레이어](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
