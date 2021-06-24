---
description: 캐비닛 재료는 캐비닛 스타일 파일(.vnc 파일 확장명), 패라메트릭 레이아웃 정의 및 캐비닛 전면을 렌더링하는 데 필요한 기타 정보와 함께 캐비닛의 사진 표현을 포함하는 특수 데이터 파일을 지정합니다.
solution: Experience Manager
title: 캐비닛
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: cdb3ed5e-c396-483d-aea0-2b3f24efe56e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 5%

---

# 캐비닛{#cabinets}

캐비닛 재료는 캐비닛 스타일 파일(.vnc 파일 확장명), 패라메트릭 레이아웃 정의 및 캐비닛 전면을 렌더링하는 데 필요한 기타 정보와 함께 캐비닛의 사진 표현을 포함하는 특수 데이터 파일을 지정합니다.

[!DNL vnc] 파일들은 반복 가능한 목재 그레인 텍스처를 포함할 수도 있고 또는 텍스처는 제2 인수를 통해 외부로 제공할 수  `src=`있습니다. 특정 [!DNL vnc] 파일은 캐비닛 전선의 선택된 영역을 색상화하거나 텍스트화할 수 있습니다(일반적으로 라미네이트 캐비닛 스타일에 사용됨).

캐비닛 재료는 캐비닛 객체에만 적용할 수 있습니다.

<table id="table_0B16200886FE4DFEBB1E4BE8FBA67EE4"> 
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
   <td colname="col2"> <p>캐비닛 스타일 파일;필수 여부. </p> </td> 
   <td colname="col3"> <p>없음. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>선택적 텍스처 이미지 파일(<span class="codeph"> src= </span>에 대한 두 번째 값). </p> </td> 
   <td colname="col3"> <p>없음. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res=  </span> </a> </p> </td> 
   <td colname="col2"> <p>텍스처 해상도(선택 사항)입니다. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::resolution  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> color=  </span> </a> </p> </td> 
   <td colname="col2"> <p>캐비닛 및/또는 텍스처에 색상을 지정합니다. </p> </td> 
   <td colname="col3"> <p>없음. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp=  </span> </a> </p> </td> 
   <td colname="col2"> <p>선명하게 하기. </p> </td> 
   <td colname="col3"> <p>0(선명하게 없음) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-flags.md#reference-3a4844f0f21346d79e6508aaad9a9ac9" type="reference" format="dita" scope="local"> <span class="codeph"> 플래그=  </span> </a> </p> </td> 
   <td colname="col2"> <p>특수 렌더링 플래그. </p> </td> 
   <td colname="col3"> <p>0(플래그 없음) </p> </td> 
  </tr> 
 </tbody> 
</table>
