---
description: 비네팅을 제작하여 거의 3D 반사 데이터를 포함할 수 있습니다.
seo-description: 비네팅을 제작하여 거의 3D 반사 데이터를 포함할 수 있습니다.
seo-title: 반사
solution: Experience Manager
title: 반사
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6d86f566-0f02-4304-8a6c-08b1a2e9c72e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 3%

---


# 반사{#reflections}

비네팅을 제작하여 거의 3D 반사 데이터를 포함할 수 있습니다.

이렇게 작성되면 다음 재료 속성을 사용하여 재료의 반사 서피스 속성을 정의합니다.

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
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a" type="reference" format="dita" scope="local"> <span class="codeph"> glossmap=  </span> </a> </p> </td> 
   <td> <p>광택 변형(회색 음영 이미지) </p> </td> 
   <td> <p>없음 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180" type="reference" format="dita" scope="local"> <span class="codeph"> rough=  </span> </a> </p> </td> 
   <td> <p>표면 거칠음 </p> </td> 
   <td> <p>40% </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35" type="reference" format="dita" scope="local"> <span class="codeph"> type=</span> </a> </p> </td> 
   <td> <p>질감 유형 </p> </td> 
   <td> <p>0(알 수 없음) </p> </td> 
  </tr> 
 </tbody> 
</table>

렌더러는 `type=`에 따라 `gloss=` 및 `rough=` 속성의 범위를 조정합니다. 직물과 같은 일부 유형의 재료는 일반적으로 돌이나 메탈과 같은 재질 유형보다 덜 반사되며, 한 재질을 위해 지정된 동일한 광택 양이 다른 재질과 다른 반사 효과를 냅니다. `gloss=`및 거칠게 하기(지정하지 않았거나 0으로 설정된 경우 `type=` 는 상당히 넓은 색상 영역을 가집니다.

`glossmap=` 픽셀 단위로 재질의 매끄러움을 제어하는 데 사용할 수 있습니다.
