---
description: 픽셀 위치별로 개체를 선택합니다.
seo-description: 픽셀 위치별로 개체를 선택합니다.
seo-title: sel
solution: Experience Manager
title: sel
topic: Scene7 Image Serving - Image Rendering API
uuid: 2a679284-9da4-44b6-b495-8e1a47296e7c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# sel{#sel}

픽셀 위치별로 개체를 선택합니다.

` sel= *``*, *``*[, *`xylevel`*]`

<table id="simpletable_247FF35D791C43D3AB433B8CF49F8C91"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> x,y </span> </p> </td> 
  <td class="stentry"> <p>위치 좌표를 픽셀 단위(int, int)로 선택합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 레벨 </span> </p> </td> 
  <td class="stentry"> <p>그룹 수준(int). </p> </td> 
 </tr> 
</table>

로 지정된 픽셀 좌표에서 그룹이나 개체를 선택하고 새 MSS를 *`x, y`* 시작합니다. 선택 가능한 개체가 선택 위치에 없거나, 선택 위치가 유효하지 않으면 에 의해 지정된 작업이 `attribute::OnFailSel` 수행됩니다.

*`level`* 가장 바깥쪽 그룹을 선택할지 또는 중첩된 그룹이나 개체로 드릴다운할지를 지정합니다. 을 지정하지 *`level`* 않으면 가장 바깥쪽 그룹이 선택됩니다. 1로 설정하면 가장 바깥쪽 그룹 아래의 한 그룹 수준을 선택할 수 있습니다. 선택되는 가장 안쪽의 개체나 그룹을 선택하려면 큰 숫자(예: 99)로 설정합니다.

## 속성 {#section-8f27e84d88734a62a5e398e0c9972bdc}

선택 명령;MSS 구분 기호. 개체 선택은 `obj=` 또는 에서 다른 개체를 선택할 때까지 지속됩니다 `sel=`.

*`x, y`* 는 0, 0(이미지의 왼쪽 위 모서리) - *`wid`*-1, *`hei`*-1(이미지의 아래쪽, 오른쪽 모서리) 범위에 있어야 하며 *`wid`* 이 범위는 확대되지 않은 비네팅 보기의 *`hei`* 크기입니다.

지정된 경우 0보다 커야 *`level`* 합니다.

## 기본값 {#section-e13c705a3e76468894b4ec190ed8a893}

없음 *`x, y`*. *`level`* 기본값은 0입니다.

## 참조 {#section-486842570b4e4bf895f6ccc172ebd8b2}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) , [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)[, attribute::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
