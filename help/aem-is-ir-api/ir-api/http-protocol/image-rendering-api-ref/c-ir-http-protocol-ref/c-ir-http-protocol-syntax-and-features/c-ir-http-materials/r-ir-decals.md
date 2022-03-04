---
title: 디칼
description: 그림, 티셔츠 인쇄, 수 또는 인쇄 로고와 같은 의복 구조가 100장 재료입니다. 또한, 영역 러그, 벽걸이형 아트, 간판 등과 같이 내부 또는 외부 응용 프로그램에서 사용되는 반복이 가능한 평면 객체를 포함합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 07190abd-9f6f-46b5-bf77-cd97c48fc9be
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 3%

---

# 디칼{#decals}

그림, 티셔츠 인쇄, 수 또는 인쇄 로고와 같은 의복 구조가 100장 재료입니다. 또한, 영역 러그, 벽걸이형 아트, 간판 등과 같이 내부 또는 외부 응용 프로그램에서 사용되는 반복이 가능한 평면 객체를 포함합니다.

MSS에 지정된 경우, 재료는 10차 MSS로 간주됩니다. 십진수 은 일반적으로 RGBA 이미지입니다. 이때 알파 채널은 십자의 모양을 정의합니다.

&#39;텍스처 없음&#39; 플래그가 설정되지 않은 경우 각각의 플랫, 순선, 스케치, 평면 또는 벽 객체에 한 개의 십분위수를 적용할 수 있습니다. 데콜을 정렬하여 대상에 데콜이 적용됩니다 `anchor=` 비네팅 개체의 decal 원점 사용 그 위치는 `pos=`.

디칼(decal) 재질이 두께를 정의하고 비네팅(vignette) 객체가 광 벡터를 정의하면 그림자(drop shadow)가 렌더링됩니다.

<table id="table_3F119BC9B7654FD092826A34F5827268"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
   <th colname="col3" class="entry"> <p>기본값 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>이미지(일반적으로 알파 사용); 필수 여부. </p> </td> 
   <td colname="col3"> <p>없음. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988" type="reference" format="dita" scope="local"> <span class="codeph"> size= </span> </a> </p> </td> 
   <td colname="col2"> <p>전체 너비, 높이 및 두께(그림자) </p> </td> 
   <td colname="col3"> <p> <span class="varname"> imageWidth </span> x <span class="codeph"> res </span>, <span class="varname"> imageHeight </span> x <span class="codeph"> res, 0 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>텍스처 해상도(size=를 지정하면 무시됨). </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::resolution </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> 앵커= </span> </a> </p> </td> 
   <td colname="col2"> <p>십진수 정렬 점입니다. </p> </td> 
   <td colname="col3"> <p>이미지 센터 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8" type="reference" format="dita" scope="local"> <span class="codeph"> pos= </span> </a> </p> </td> 
   <td colname="col2"> <p>상대적 십진수 위치입니다. </p> </td> 
   <td colname="col3"> <p>0, 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-opac.md#reference-136b8563da714313a9e103f4ce179c5b" type="reference" format="dita" scope="local"> <span class="codeph"> opac= </span> </a> </p> </td> 
   <td colname="col2"> <p>불투명. </p> </td> 
   <td colname="col3"> <p>100% </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span> </a> </td> 
   <td colname="col2"> <p>선명하게 하기. </p> </td> 
   <td colname="col3"> <p>0(선명하게 없음) </p> </td> 
  </tr> 
 </tbody> 
</table>
