---
title: rs
description: 고급 렌더링 설정. 현재 선택 영역을 렌더링할 때 적용할 고급 렌더링 설정을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 419baeb7-e06e-4753-a487-a1f407845f6d
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 3%

---

# rs{#rs}

고급 렌더링 설정. 현재 선택 영역을 렌더링할 때 적용할 고급 렌더링 설정을 지정합니다.

`rs= *`val`*`

<table id="simpletable_4B028996E5824FC18B9749D1A6A3C2E3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>렌더링 설정 문자열. </p></td> 
 </tr> 
</table>

렌더링 모양을 미세 조정하는 데 사용됩니다. 렌더링 설정 문자열을 만들려면 비네팅 작성 도구(Dynamic Media 이미지 작성 패키지의 일부)의 렌더링 기능을 사용하십시오.

## 속성 {#section-9a2b2228789046658cb80eddf343af75}

재질 속성입니다.

## 기본값 {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings`.

## 예 {#section-47e4811882574441a4d517e42a35f352}

이미지 작성에서 몇 가지 실험을 수행한 결과, USM(unsharp-masking)이 제공된 응용 프로그램과 재료에 대해 정확한 선명도를 제공한다고 판명되었습니다. USM을 구성하는 렌더링 설정 문자열이 `rs=` 이 자료에 사용할 명령:

`…&rs=U2V20W50X2&…`

## 참조 {#section-930116e735024a008c994547ba36ee40}

[catalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
