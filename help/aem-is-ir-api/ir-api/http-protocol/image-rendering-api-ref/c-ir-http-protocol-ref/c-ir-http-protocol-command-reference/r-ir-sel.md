---
title: sel
description: 픽셀 위치별로 객체를 선택합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fac33287-ebcc-4995-b968-ac377065fdd4
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---

# sel{#sel}

픽셀 위치별로 객체를 선택합니다.

` sel= *`x`*, *`y`*[, *`수준`*]`

<table id="simpletable_247FF35D791C43D3AB433B8CF49F8C91"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> x,y </span> </p> </td> 
  <td class="stentry"> <p>위치 좌표를 픽셀 단위로 선택합니다(int, int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 레벨 </span> </p> </td> 
  <td class="stentry"> <p>그룹 수준(int). </p> </td> 
 </tr> 
</table>

지정된 픽셀 좌표에서 그룹이나 오브젝트를 선택합니다. *`x, y`* 새로운 MSS를 시작합니다. 선택 가능한 객체가 피킹 위치에 없거나 피킹 위치가 유효하지 않은 경우 `attribute::OnFailSel` 사용 중입니다.

*`level`* 가장 바깥쪽 그룹을 선택할지 또는 중첩된 그룹이나 개체로 드릴다운할지 여부를 지정합니다. If *`level`* 을 지정하지 않으면 가장 바깥쪽 그룹이 선택됩니다. 가장 바깥쪽 그룹 아래에 있는 그룹 수준을 선택하려면 1로 설정합니다. 가장 안쪽의 선택 가능한 개체 또는 그룹을 선택하려면 큰 숫자(예: 99)로 설정하십시오.

## 속성 {#section-8f27e84d88734a62a5e398e0c9972bdc}

선택 명령, MSS 구분 기호. 다음 중 하나를 사용하여 다른 객체를 선택할 때까지 객체 선택은 지속됩니다. `obj=` 또는 `sel=`.

*`x, y`* 의 범위는 0, 0(이미지의 왼쪽 상단 모서리)이어야 합니다. *`wid`*-1, *`hei`*-1(이미지의 하단, 오른쪽 모서리), 여기서 *`wid`* 및 *`hei`* 는 크기 조정되지 않은 비네팅 보기의 크기입니다.

지정하면, *`level`* 은(는) 0 이상이어야 합니다.

## 기본값 {#section-e13c705a3e76468894b4ec190ed8a893}

다음에 대해 없음: *`x, y`*. *`level`* 기본값은 0입니다.

## 참조 {#section-486842570b4e4bf895f6ccc172ebd8b2}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) , [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f), [attribute::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
