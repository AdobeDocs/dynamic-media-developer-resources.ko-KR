---
description: 1000만 개의 자료에는 앱 리큐어, 티셔츠 인쇄, 수 선 또는 인쇄 로고, 영역 러그, 벽면 아트, 기호 등과 같은 내부 또는 외부 어플리케이션에서 사용되는 반복 가능한 플랫 오브젝트도 포함되어 있습니다.
seo-description: 1000만 개의 자료에는 앱 리큐어, 티셔츠 인쇄, 수 선 또는 인쇄 로고, 영역 러그, 벽면 아트, 기호 등과 같은 내부 또는 외부 어플리케이션에서 사용되는 반복 가능한 플랫 오브젝트도 포함되어 있습니다.
seo-title: 디칼스
solution: Experience Manager
title: 디칼스
topic: Scene7 Image Serving - Image Rendering API
uuid: 6e64f382-f15f-4018-b00c-4fd21a4ebc8c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 2%

---


# decals{#decals}

1000만 개의 자료에는 앱 리큐어, 티셔츠 인쇄, 수 선 또는 인쇄 로고, 영역 러그, 벽면 아트, 기호 등과 같은 내부 또는 외부 어플리케이션에서 사용되는 반복 가능한 플랫 오브젝트도 포함되어 있습니다.

디칼 MSS에 자료의 이름을 지정한 경우 디캘로 간주됩니다. 일반적으로 RGBA 이미지이며 알파 채널이 십자의 모양을 정의합니다.

&#39;텍스처 없음&#39; 플래그가 설정되어 있지 않은 한 각각의 평면, 순선, 스케치, 평면 또는 벽 오브젝트에 하나의 설명을 적용할 수 있습니다. 비네팅 객체의 디폴트 원점을 사용하여 디캘의 `anchor=`을 정렬하여 오브젝트에 디캘이 적용됩니다. 위치는 `pos=`으로 추가로 조정할 수 있습니다.

그림자가 디컬한 재질이 두께를 정의하고 비네팅 객체가 라이트 벡터를 정의하면 렌더링됩니다.

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>이미지(일반적으로 알파 포함);필요합니다. </p> </td> 
   <td colname="col3"> <p>없음. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988" type="reference" format="dita" scope="local"> <span class="codeph"> size=  </span> </a> </p> </td> 
   <td colname="col2"> <p>폭, 높이 및 두께 감소(그림자의 경우) </p> </td> 
   <td colname="col3"> <p> <span class="varname"> imageWidth  </span> x  <span class="codeph"> res  </span>,  <span class="varname"> imageHeight  </span> x  <span class="codeph"> res, 0  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res=  </span> </a> </p> </td> 
   <td colname="col2"> <p>텍스처 해상도(size=가 지정된 경우 무시됨). </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> 속성::Resolution  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> anchor=  </span> </a> </p> </td> 
   <td colname="col2"> <p>디컬링 점. </p> </td> 
   <td colname="col3"> <p>이미지 센터. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8" type="reference" format="dita" scope="local"> <span class="codeph"> pos=  </span> </a> </p> </td> 
   <td colname="col2"> <p>상대적 decal 위치입니다. </p> </td> 
   <td colname="col3"> <p>0, 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-opac.md#reference-136b8563da714313a9e103f4ce179c5b" type="reference" format="dita" scope="local"> <span class="codeph"> opac=  </span> </a> </p> </td> 
   <td colname="col2"> <p>불투명도 감소. </p> </td> 
   <td colname="col3"> <p>100% </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp=  </span> </a> </td> 
   <td colname="col2"> <p>선명하게 하기. </p> </td> 
   <td colname="col3"> <p>0(선명하게 하지 않음) </p> </td> 
  </tr> 
 </tbody> 
</table>

