---
title: 벽 테두리
description: 물질이 벽 경계 MSS(sub=3..5로 도입됨)에 지정되는 경우 벽 경계로 간주됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e11c38d0-8255-4363-ae60-f47be37a1495
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 5%

---

# 벽 테두리{#wall-borders}

물질이 벽 경계 MSS(sub=3..5로 도입됨)에 지정되는 경우 벽 경계로 간주됩니다.

벽 테두리 텍스처 이미지들은 테두리의 형상을 정의하기 위해 알파 채널을 포함할 수 있다. 벽 경계는 벽 객체에만 적용할 수 있습니다.

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>반복 가능한 텍스처 이미지, 필수 </p> </td> 
   <td colname="col3"> <p>없음 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>텍스처 해상도 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::Resolution </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> 앵커= </span> </a> </p> </td> 
   <td colname="col2"> <p>수평 텍스쳐 정렬(y 값은 무시됨) </p> </td> 
   <td colname="col3"> <p>0(왼쪽 이미지 가장자리) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span> </a> </p> </td> 
   <td colname="col2"> <p>선명하게 하기 </p> </td> 
   <td colname="col3"> <p>0(선명하게 하기 없음) </p> </td> 
  </tr> 
 </tbody> 
</table>
