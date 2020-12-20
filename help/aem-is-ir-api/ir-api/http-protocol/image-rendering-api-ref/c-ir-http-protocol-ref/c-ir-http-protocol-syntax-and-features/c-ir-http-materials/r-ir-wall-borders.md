---
description: 자료는 벽 테두리 MSS(sub=3.5와 함께 도입됨)에 지정된 경우 벽 테두리로 간주됩니다.
seo-description: 자료는 벽 테두리 MSS(sub=3.5와 함께 도입됨)에 지정된 경우 벽 테두리로 간주됩니다.
seo-title: 벽 테두리
solution: Experience Manager
title: 벽 테두리
topic: Scene7 Image Serving - Image Rendering API
uuid: 40acd667-5e8b-4425-b44a-0681e608d189
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 4%

---


# 벽 테두리{#wall-borders}

자료는 벽 테두리 MSS(sub=3.5와 함께 도입됨)에 지정된 경우 벽 테두리로 간주됩니다.

벽 테두리 텍스처 이미지에는 테두리 모양을 정의하는 알파 채널이 포함될 수 있습니다. 벽 테두리는 벽 개체에만 적용할 수 있습니다.

<table id="table_906C5CC4CADF4024AA0E29544AF48080"> 
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
   <td colname="col2"> <p>반복 가능한 텍스처 이미지;required </p> </td> 
   <td colname="col3"> <p>없음 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res=  </span> </a> </p> </td> 
   <td colname="col2"> <p>텍스처 해상도 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> 속성::Resolution  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> anchor=  </span> </a> </p> </td> 
   <td colname="col2"> <p>수평 텍스처 정렬(y 값은 무시됨) </p> </td> 
   <td colname="col3"> <p>0(왼쪽 이미지 가장자리) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp=  </span> </a> </p> </td> 
   <td colname="col2"> <p>선명하게 하기 </p> </td> 
   <td colname="col3"> <p>0(선명하게 하지 않음) </p> </td> 
  </tr> 
 </tbody> 
</table>

