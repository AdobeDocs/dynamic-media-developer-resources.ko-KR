---
title: 플래그
description: 플래그를 적용합니다. 추가 렌더링 옵션을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0c3f65e-2dec-4c35-8df4-8d111e81f3f0
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 5%

---

# 플래그 {#flags}

플래그를 적용합니다. 추가 렌더링 옵션을 지정합니다.

`flags= *`val`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>플래그 값. </p></td> 
 </tr> 
</table>

현재 캐비닛 재료에만 사용됩니다.

`flags=0` (기본값) 상위 캐비닛에 견고한 도어가 표시됩니다.

`flags=1` 유리 도어로 위쪽 캐비닛을 렌더링합니다(유리 도어로 만든 경우).

## 속성 {#section-a2b00d7bb15e449ea85178acb92d8285}

재료 속성입니다. 캐비닛 자료가 없거나 대상 캐비닛 객체가 유리 문을 허용하지 않는 경우에는 무시됩니다.

## 기본값 {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` 유리문이 없어서
