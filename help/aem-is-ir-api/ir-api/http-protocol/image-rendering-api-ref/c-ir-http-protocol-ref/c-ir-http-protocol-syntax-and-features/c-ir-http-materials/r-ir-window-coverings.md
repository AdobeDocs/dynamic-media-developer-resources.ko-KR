---
description: 창문 덮는 재료는 부드러운 창문 커버링(커튼용 커튼용 커튼용 커튼용), 하드창 커버(차양 및 블라인드)가 모두 포함되어 있습니다.
seo-description: 창문 덮는 재료는 부드러운 창문 커버링(커튼용 커튼용 커튼용 커튼용), 하드창 커버(차양 및 블라인드)가 모두 포함되어 있습니다.
seo-title: 창 커버
solution: Experience Manager
title: 창 커버
topic: Scene7 Image Serving - Image Rendering API
uuid: 3d74466a-b7c3-43b0-9b0b-f8bb809e2773
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Window coverings{#window-coverings}

창문 덮는 재료는 부드러운 창문 커버링(커튼용 커튼용 커튼용 커튼용), 하드창 커버(차양 및 블라인드)가 모두 포함되어 있습니다.

창 덮기 재료는 마스크, 조명, 레이아웃 및 창 덮기를 정의하는 텍스처 데이터가 들어 있는 비네팅과 유사한 특수 데이터 파일 *(* 파일 확장명)을 덮는 [!DNL .vnw] 창을 지정합니다.

[!DNL vnw] 파일에는 창 덮기의 색상 및 텍스처(패브릭)가 포함되지 않습니다. 이 정보는 반복 가능한 텍스처와 유사하게 별도로 지정됩니다.

창 커버링 재료는 겹쳐진 개체인 창 커버링 프레임 개체에만 적용할 수 있습니다.

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span></a> </p> </td> 
   <td colname="col2"> <p>윈도우 커버 스타일 파일;필수. </p> </td> 
   <td colname="col3"> <p>없음. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span></a> </p> </td> 
   <td colname="col2"> <p>텍스처 이미지 파일( <span class="codeph"> src= </span>의 두 번째 값). </p> </td> 
   <td colname="col3"> <p>없음. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span></a> </p> </td> 
   <td colname="col2"> <p>텍스처 해상도. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> 속성::Resolution </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> repeat= </span></a> </p> </td> 
   <td colname="col2"> <p>반복 모드. </p> </td> 
   <td colname="col3"> <p>0(직선 반복) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> 색상= </span></a> </p> </td> 
   <td colname="col2"> <p>단색(또는 색상 텍스처). </p> </td> 
   <td colname="col3"> <p>128 (중립 회색) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span></a> </p> </td> 
   <td colname="col2"> <p>선명하게 하기. </p> </td> 
   <td colname="col3"> <p>0(선명하게 하지 않음) </p> </td> 
  </tr> 
 </tbody> 
</table>

