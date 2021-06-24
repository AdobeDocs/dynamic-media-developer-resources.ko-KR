---
description: 고급 렌더링 설정. 현재 선택 항목을 렌더링할 때 적용할 고급 렌더링 설정을 지정합니다.
solution: Experience Manager
title: rs
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 419baeb7-e06e-4753-a487-a1f407845f6d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 4%

---

# rs{#rs}

고급 렌더링 설정. 현재 선택 항목을 렌더링할 때 적용할 고급 렌더링 설정을 지정합니다.

`rs= *`val`*`

<table id="simpletable_4B028996E5824FC18B9749D1A6A3C2E3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>설정 문자열을 렌더링합니다. </p></td> 
 </tr> 
</table>

렌더링 모양을 세밀하게 조정하는 데 사용됩니다. Dynamic Media 이미지 작성 패키지의 일부 비네팅 작성 도구의 렌더링 기능을 사용하여 렌더링 설정 문자열을 만듭니다.

## 속성 {#section-9a2b2228789046658cb80eddf343af75}

재료 속성입니다.

## 기본값 {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings`.

## 예 {#section-47e4811882574441a4d517e42a35f352}

이미지 작성에서 몇 가지 실험을 거친 후 USM(언샵 마스킹)이 주어진 응용 프로그램 및 재료에 대해 정확한 선명하게 하기 위한 양을 제공하는 것으로 결정됩니다. USM을 구성하는 렌더링 설정 문자열은 이 자료와 함께 사용하도록 `rs=` 명령에 복사됩니다.

`…&rs=U2V20W50X2&…`

## 참조 {#section-930116e735024a008c994547ba36ee40}

[카탈로그::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
