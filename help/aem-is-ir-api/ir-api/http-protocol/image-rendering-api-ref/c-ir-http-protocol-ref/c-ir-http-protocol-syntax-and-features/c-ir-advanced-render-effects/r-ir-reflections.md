---
title: 반사
description: 거의 3D 반사 데이터를 포함하도록 비네팅을 작성할 수 있습니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f67ede68-03c0-461f-a16d-a308f76fd24c
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 3%

---

# 반사{#reflections}

거의 3D 반사 데이터를 포함하도록 비네팅을 작성할 수 있습니다.

이렇게 작성되면 다음 재료 속성을 사용하여 재료의 반사 서피스 특성을 정의합니다.

<table id="table_8769C726A17E412FB41F7CB87690B1FE"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>속성 </p> </th> 
   <th class="entry"> <p>설명 </p> </th> 
   <th class="entry"> <p>기본값 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca" type="reference" format="dita" scope="local"> <span class="codeph"> 광택=</span> </a> </p> </td> 
   <td> <p>표면 광택 </p> </td> 
   <td> <p>비네팅에서 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a" type="reference" format="dita" scope="local"> <span class="codeph"> glossmap= </span> </a> </p> </td> 
   <td> <p>광택 변형(회색 음영 이미지) </p> </td> 
   <td> <p>없음 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180" type="reference" format="dita" scope="local"> <span class="codeph"> rough= </span> </a> </p> </td> 
   <td> <p>표면 거칠기 </p> </td> 
   <td> <p>40% </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35" type="reference" format="dita" scope="local"> <span class="codeph"> type=</span> </a> </p> </td> 
   <td> <p>재료 유형 </p> </td> 
   <td> <p>0 (알 수 없음) </p> </td> 
  </tr> 
 </tbody> 
</table>

렌더러는 `gloss=` 및 `rough=` 속성에 따라 `type=`. 직물과 같은 일부 재료는 석재나 금속과 같은 재질보다 반사가 적다. 또한, 동일한 광택이 한 광택에 대해 지정되면 다른 광택과 다른 반사 효과가 발생한다. 속성 `gloss=` 그리고 거칠기는 `type=` 가 지정되지 않았거나 이 `0`.

`glossmap=` 재료의 광택성을 픽셀 단위로 제어하는 데 사용됩니다.
