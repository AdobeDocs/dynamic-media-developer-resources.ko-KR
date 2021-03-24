---
description: 픽셀 위치별로 개체를 선택합니다.
solution: Experience Manager
title: sel
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 2%

---


# sel{#sel}

픽셀 위치별로 개체를 선택합니다.

` sel= *``*, *``*[, *`xylevel`*]`

<table id="simpletable_247FF35D791C43D3AB433B8CF49F8C91"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> x,y  </span> </p> </td> 
  <td class="stentry"> <p>위치 좌표를 픽셀 단위(int, int)로 선택합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 레벨 </span> </p> </td> 
  <td class="stentry"> <p>그룹 수준(int). </p> </td> 
 </tr> 
</table>

*`x, y`*&#x200B;에 의해 지정된 픽셀 좌표로 그룹 또는 개체를 선택하고 새 MSS를 시작합니다. 선택 가능한 객체가 선택 위치에 없거나 선택 위치가 유효하지 않으면 `attribute::OnFailSel`에 의해 지정된 작업이 수행됩니다.

*`level`* 가장 바깥쪽 그룹을 선택할지, 중첩된 그룹이나 개체로 드릴다운할지 여부를 지정합니다. *`level`*&#x200B;을(를) 지정하지 않으면 가장 바깥쪽 그룹이 선택됩니다. 가장 바깥쪽 그룹 아래의 한 그룹 수준을 선택하려면 1로 설정합니다. 선택 가능한 가장 안쪽의 개체나 그룹을 선택하려면 큰 숫자(예: 99)로 설정합니다.

## 속성 {#section-8f27e84d88734a62a5e398e0c9972bdc}

선택 명령;MSS 구분 기호. `obj=` 또는 `sel=` 중 하나를 사용하여 다른 개체를 선택할 때까지 개체 선택 항목은 계속 유지됩니다.

*`x, y`* 는 0, 0(이미지의 왼쪽 위 모서리) -  *`wid`*-1,  *`hei`* 1(이미지의 아래쪽, 오른쪽 모서리) 범위의 값으로, 여기서 는 크기 조절되지 않은 비네팅 보기 *`wid`* 의  *`hei`* 크기입니다.

지정한 경우 *`level`*&#x200B;은(는) 0 이상이어야 합니다.

## 기본값 {#section-e13c705a3e76468894b4ec190ed8a893}

*`x, y`*&#x200B;에 대해 없음 *`level`* 기본값은 0입니다.

## 참조 {#section-486842570b4e4bf895f6ccc172ebd8b2}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) ,  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [속성::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)  [, 속성::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
