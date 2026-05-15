---
title: 텍스트 경로
description: 텍스트 경로. textPs=와 함께 제공된 텍스트의 기준선으로 사용할 경로를 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1c515786-bbba-44d3-837e-b474af293b7e
TQID: 'https://experienceleague.adobe.com/zVKtDOaScVXM-69CquAw4cpc81Wj7X47LLxBf0RdJ6c'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 143
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

*`pathDefinition`*&#x200B;에 대한 설명을 포함한 추가 정보는 [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)을(를) 참조하십시오.

>[!NOTE]
>
>`clipPath=`과(와) 달리 하위 경로 끝에 &#39;z&#39; 또는 &#39;Z&#39;를 지정하지 않으면 텍스트 경로가 자동으로 닫히지 않습니다.

*`pathDefinition`*&#x200B;에는 여러 하위 경로가 포함될 수 있습니다. 텍스트는 지정된 순서대로 하위 경로에 렌더링됩니다.

RTF 명령 `\ql`, `\qc`, `\qr`, `\li` 및 `\ri`을(를) 사용하여 경로를 따라 렌더링된 텍스트를 배치할 수 있습니다.

## 속성 {#section-068137df436c46b9b55d271eb60e7285}

텍스트 레이어 특성(`textPs=`만 해당). 다른 레이어에서 무시됨. `layer=comp`에 대해 지정된 경우 `layer=0`에 적용됩니다. `textPs=`이(가) 있는 경우 무시됩니다.

레이어에 `textPath=`과(와) `textFlowPath=`이(가) 모두 포함된 경우 오류가 반환됩니다.

## 기본값 {#section-697b1f2cfc43498080a31327e6eb173d}

없음, 표준 텍스트 렌더링의 경우.

## 참조 {#section-3050d8f47e1d4f5c9b474dece45ea93d}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) , [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), [텍스트 레이어](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
