---
title: 하위
description: 하위 선택. 선택한 개체 또는 그룹의 다른 영역에 다른 재료를 적용하고 이전에 적용된 재료를 제거할 수 있습니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c9968fbb-c38b-4180-81be-19992fa8f347
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 6%

---

# 하위{#sub}

하위 선택. 선택한 개체 또는 그룹의 다른 영역에 다른 재료를 적용하고 이전에 적용된 재료를 제거할 수 있습니다.

`sub=0|1|2|3|4|5`

<table id="simpletable_F6BF91BD2C4B47BF8A28032E392D37F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>전체 벽을 선택합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>벽의 위쪽 절반을 선택합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>벽 아래쪽을 선택합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>위쪽 벽 테두리 영역을 선택합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>가운데 벽 테두리 영역을 선택합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>아래쪽 벽 테두리 영역을 선택합니다. </p> </td> 
 </tr> 
</table>

현재는 벽 객체에만 지원됩니다. 이전 MSS를 종료하고 지정된 하위 선택에 적용할 자료에 대한 새 MSS를 시작합니다.

벽의 나머지 절반에 대해 다른 재료가 지정되지 않은 한 위쪽이나 아래쪽벽에 지정된 재료는 전체 벽에 적용됩니다.

## 속성 {#section-b202139d6d0847cc8d520a154104ab9d}

선택 명령, MSS 구분 기호.

## 기본값 {#section-5b45a167a17c451596e4c59b7d53c368}

`sub=0`

## 참조 {#section-1a993ee24f144d4fb8baef0cc431b53b}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)
