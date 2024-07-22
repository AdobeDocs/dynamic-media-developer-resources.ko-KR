---
title: 데칼
description: 데칼 물질에는 아플리케, 티셔츠 프린트, 자수 또는 인쇄 로고와 같은 의류 구물이 포함됩니다. 또한 영역 러그, 벽걸이형 아트, 간판 등 내부 또는 외부 응용 분야에서 사용되는 반복할 수 없는 플랫 객체도 포함됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 07190abd-9f6f-46b5-bf77-cd97c48fc9be
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 1%

---

# 데칼{#decals}

데칼 물질에는 아플리케, 티셔츠 프린트, 자수 또는 인쇄 로고와 같은 의류 구물이 포함됩니다. 또한 영역 러그, 벽걸이형 아트, 간판 등 내부 또는 외부 응용 분야에서 사용되는 반복할 수 없는 플랫 객체도 포함됩니다.

물질이 데칼 MSS에 지정되어 있으면 데칼로 간주됩니다. 데칼은 일반적으로 RGBA 이미지이며 알파 채널은 데칼의 모양을 정의합니다.

각 플랫, 플로우 라인, 스케치, 평면 또는 벽 개체에 하나의 데칼을 적용할 수 있습니다(&#39;텍스처 없음&#39; 플래그가 설정되지 않은 경우). 데칼의 `anchor=`을(를) 비네팅 개체의 데칼 원점과 정렬하여 개체에 데칼이 적용됩니다. `pos=`(으)로 위치를 추가로 조정할 수 있습니다.

데칼 재료가 두께를 정의하고 비네팅 오브젝트가 라이트 벡터를 정의하는 경우 그림자가 렌더링됩니다.

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
   <td colname="col2"> <p>이미지(일반적으로 알파 사용), 필수 필드입니다. </p> </td> 
   <td colname="col3"> <p>없음. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988" type="reference" format="dita" scope="local"> <span class="codeph"> 크기= </span> </a> </p> </td> 
   <td colname="col2"> <p>데칼 너비, 높이 및 두께(그림자). </p> </td> 
   <td colname="col3"> <p> <span class="varname"> imageWidth </span> x <span class="codeph"> res </span>, <span class="varname"> imageHeight </span> x <span class="codeph"> res, 0 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>텍스처 해상도(size=가 지정된 경우 무시됨). </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> 특성::해상도 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> 앵커= </span> </a> </p> </td> 
   <td colname="col2"> <p>데칼 정렬 점. </p> </td> 
   <td colname="col3"> <p>이미지 센터입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8" type="reference" format="dita" scope="local"> <span class="codeph"> pos= </span> </a> </p> </td> 
   <td colname="col2"> <p>상대적 데칼 위치입니다. </p> </td> 
   <td colname="col3"> <p>0, 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-opac.md#reference-136b8563da714313a9e103f4ce179c5b" type="reference" format="dita" scope="local"> <span class="codeph"> opac= </span> </a> </p> </td> 
   <td colname="col2"> <p>데칼 불투명도. </p> </td> 
   <td colname="col3"> <p>100% </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> 선명하게= </span> </a> </td> 
   <td colname="col2"> <p>선명하게 하기. </p> </td> 
   <td colname="col3"> <p>0(선명하게 하기 없음) </p> </td> 
  </tr> 
 </tbody> 
</table>
