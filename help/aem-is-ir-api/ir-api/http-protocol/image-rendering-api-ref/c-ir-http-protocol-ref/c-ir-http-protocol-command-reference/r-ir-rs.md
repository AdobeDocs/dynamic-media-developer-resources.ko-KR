---
description: 고급 렌더링 설정. 현재 선택 항목을 렌더링할 때 적용할 고급 렌더링 설정을 지정합니다.
seo-description: 고급 렌더링 설정. 현재 선택 항목을 렌더링할 때 적용할 고급 렌더링 설정을 지정합니다.
seo-title: rs
solution: Experience Manager
title: rs
topic: Scene7 Image Serving - Image Rendering API
uuid: 4ff7fcb4-a10a-4e82-80a1-edf79ae1f717
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 3%

---


# rs{#rs}

고급 렌더링 설정. 현재 선택 항목을 렌더링할 때 적용할 고급 렌더링 설정을 지정합니다.

`rs= *`val`*`

<table id="simpletable_4B028996E5824FC18B9749D1A6A3C2E3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>렌더링 설정 문자열. </p></td> 
 </tr> 
</table>

렌더링 모양을 미세 조정하는 데 사용됩니다. 렌더링 설정 문자열을 만들려면 비네팅 제작 도구(Scene7 이미지 제작 패키지의 일부)의 렌더링 기능을 사용합니다.

## 속성 {#section-9a2b2228789046658cb80eddf343af75}

재료 속성.

## 기본값 {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings`.

## 예 {#section-47e4811882574441a4d517e42a35f352}

이미지 작성에서 몇 가지 실험을 거친 후 USM(언샵 마스킹)이 주어진 애플리케이션 및 자료에 대해 선명하게 하기 정확한 양을 제공하는 것으로 결정됩니다. USM을 구성하는 렌더링 설정 문자열이 이 자료에 사용할 `rs=` 명령에 복사됩니다.

`…&rs=U2V20W50X2&…`

## 참조 {#section-930116e735024a008c994547ba36ee40}

[카탈로그::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
