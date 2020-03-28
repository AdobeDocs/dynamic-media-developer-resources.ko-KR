---
description: 하위 선택. 선택한 개체 또는 그룹의 다른 영역에 다른 자료를 적용할 수 있을 뿐만 아니라 이전에 적용된 자료를 제거할 수 있습니다.
seo-description: 하위 선택. 선택한 개체 또는 그룹의 다른 영역에 다른 자료를 적용할 수 있을 뿐만 아니라 이전에 적용된 자료를 제거할 수 있습니다.
seo-title: sub
solution: Experience Manager
title: sub
topic: Scene7 Image Serving - Image Rendering API
uuid: cb9f4dc5-9d89-483a-ae72-b9076b27c57e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# sub{#sub}

하위 선택. 선택한 개체 또는 그룹의 다른 영역에 다른 자료를 적용할 수 있을 뿐만 아니라 이전에 적용된 자료를 제거할 수 있습니다.

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
  <td class="stentry"> <p>벽의 하단을 선택합니다. </p> </td> 
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

현재 벽 객체에만 지원됩니다. 이전 MSS를 종료하고 지정된 하위 선택에 적용할 자료에 대한 새 MSS를 시작합니다.

벽의 다른 반쪽에도 다른 재료를 지정하지 않은 경우 위쪽 또는 아래쪽 벽에 지정된 자료가 전체 벽에 적용됩니다.

## 속성 {#section-b202139d6d0847cc8d520a154104ab9d}

선택 명령;MSS 구분 기호.

## 기본값 {#section-5b45a167a17c451596e4c59b7d53c368}

`sub=0`

## 참조 {#section-1a993ee24f144d4fb8baef0cc431b53b}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)
