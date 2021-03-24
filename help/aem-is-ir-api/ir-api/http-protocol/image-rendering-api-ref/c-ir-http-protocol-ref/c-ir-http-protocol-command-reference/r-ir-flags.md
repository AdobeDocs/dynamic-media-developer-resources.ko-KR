---
description: 플래그를 적용합니다. 추가 렌더링 옵션을 지정합니다.
solution: Experience Manager
title: 플래그
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 5%

---


# 플래그{#flags}

플래그를 적용합니다. 추가 렌더링 옵션을 지정합니다.

`flags= *`val`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>플래그 값을 참조하십시오. </p></td> 
 </tr> 
</table>

현재 캐비닛 재료에만 사용됩니다.

`flags=0` (기본값)는 위쪽 캐비닛에 단색 문이 있는 것을 렌더링합니다.

`flags=1` 유리 문이 있는 위쪽 캐비닛을 렌더링합니다(비네팅을 유리 문으로 만든 경우).

## 속성 {#section-a2b00d7bb15e449ea85178acb92d8285}

재료 속성. 캐비닛 자료가 없거나 대상 캐비닛 객체가 유리 문을 허용하지 않는 경우 무시됩니다.

## 기본값 {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` 유리문 없이
