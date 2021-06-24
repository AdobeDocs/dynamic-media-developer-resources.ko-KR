---
description: 창문 덮개재로는 부드러운 창문 커버(커튼월, 장식, 카페 커튼)와 하드윈도우 커버(차양 및 블라인드)가 모두 있다.
solution: Experience Manager
title: 창문 커버
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: ce6543a1-2438-4661-95bf-ff3d956013bc
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 3%

---

# 창문 커버{#window-coverings}

창문 덮개재로는 부드러운 창문 커버(커튼월, 장식, 카페 커튼)와 하드윈도우 커버(차양 및 블라인드)가 모두 있다.

창 관련 자료는 *창 커버 스타일 파일*( [!DNL .vnw] 파일 확장명)을 지정합니다. 이 특수 데이터 파일은 마스크, 조명, 레이아웃 및 창 덮개를 정의하는 텍스처 데이터를 포함합니다.

[!DNL vnw] 이 파일에는 창 덮개의 색상 및 텍스처(패브릭)가 포함되지 않습니다. 이 정보는 반복 가능한 텍스처와 유사하며 별도로 지정됩니다.

창 덮개 재료는 겹쳐진 오브젝트인 창 커버 프레임 객체에만 적용할 수 있습니다.

<table id="table_545865B054E84592BDAEDA57DBFAE9B3"> 
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
   <td colname="col2"> <p>스타일 파일을 덮는 창필수 여부. </p> </td> 
   <td colname="col3"> <p>없음. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>텍스처 이미지 파일(<span class="codeph"> src= </span>에 대한 두 번째 값). </p> </td> 
   <td colname="col3"> <p>없음. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res=  </span> </a> </p> </td> 
   <td colname="col2"> <p>텍스처 해상도. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::resolution  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> 반복=  </span> </a> </p> </td> 
   <td colname="col2"> <p>반복 모드. </p> </td> 
   <td colname="col3"> <p>0(직선 반복) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> color=  </span> </a> </p> </td> 
   <td colname="col2"> <p>단색(또는 텍스처 색상)입니다. </p> </td> 
   <td colname="col3"> <p>128(중성 회색) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp=  </span> </a> </p> </td> 
   <td colname="col2"> <p>선명하게 하기. </p> </td> 
   <td colname="col3"> <p>0(선명하게 없음) </p> </td> 
  </tr> 
 </tbody> 
</table>
