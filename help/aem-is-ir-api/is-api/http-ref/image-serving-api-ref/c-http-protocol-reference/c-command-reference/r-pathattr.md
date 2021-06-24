---
description: 텍스트-경로 특성.
solution: Experience Manager
title: pathAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: fdf9274a-70d0-4692-a7a9-c108abb9ab84
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 3%

---

# pathAttr{#pathattr}

텍스트-경로 특성.

` pathAttr= *``*[, *``*[, *`directionstartPostendPos`*]]`

<table id="simpletable_EC76095316AF4F07B1DDCC0D72B814CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 방향 </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 규범  </span> |  <span class="codeph"> 역방향  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> startPos  </span> </p> </td> 
  <td class="stentry"> <p>경로에서 텍스트 시작 위치(실제 0.0..1.0). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> endPos  </span> </p> </td> 
  <td class="stentry"> <p>경로의 텍스트 끝 위치(실수 0.0..&lt;2.0). </p> </td> 
 </tr> 
</table>

첫 번째 패스 교점 근처에서 텍스트를 그리려면 `norm` 을 지정하고 마지막 교점 근처에서 시작하여 반대 방향으로 텍스트를 그리려면 `reverse` 를 지정합니다.

*`startPos`* 패스 *`endPos`* 에서 텍스트를 그릴 위치를 조정할 수 있습니다. 0.0은 패스의 첫 번째 교점에 해당하고 1.0은 마지막 교점에 해당합니다.중간 값은 첫 번째 교점과 마지막 교점 사이의 경로를 따라 거리를 나타냅니다.

## 속성 {#section-80f266da4e2549d89f022a3f9ff4584d}

레이어 속성입니다. 레이어에 `textPs=` 및 `textPath=` 명령이 포함되어 있지 않으면 무시됩니다.

*`startPos`* 0보다 크거나 같고 1.0보다 작아야  *`endPos`* 합니다. 열린 경로에 적용할 때는 1.0보다  *`startPos`* 크거나 같고, 닫힌 경로에 적용할 경우 (  *`startPos`* + 1.0)보다 작거나 같아야 합니다.

## 기본값 {#section-3e757970885c45e7b6100e78dc08626f}

`pathAttr=norm,0,1`

## 참조 {#section-b869745de1da4ef996dfda4af39ed14d}

[textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd) ,  [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
