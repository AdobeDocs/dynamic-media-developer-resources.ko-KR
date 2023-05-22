---
title: 반복 가능한 텍스처
description: 반복 가능한 텍스처에는 직물(의류 및 실내 장식 모두), 벽-벽 바닥 덮개, 벽지, 카운터탑 재료, 목재 그레인 텍스처, 루핑 및 사이딩 재료 및 기타 일반적인 텍스처와 같은 내부 및 외부 재료가 포함됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3693498b-994a-460a-8b2e-780a1482d37a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 3%

---

# 반복 가능한 텍스처{#repeatable-textures}

반복 가능한 텍스처에는 직물(의류 및 실내 장식 모두), 벽-벽 바닥 덮개, 벽지, 카운터탑 재료, 목재 그레인 텍스처, 루핑 및 사이딩 재료 및 기타 일반적인 텍스처와 같은 내부 및 외부 재료가 포함됩니다.

반복 가능한 텍스처는 플랫, 플로우 라인, 스케치, 평면, 벽 및 캐비닛 객체에 적용할 수 있습니다. 텍스처가 불가능한 오브젝트에 적용되면 오브젝트는 다음과 같이 페인트됩니다 `color=` (또는 `bgc=` if `color=` 이 지정되지 않았습니다).

소재에 텍스처가 포함되면 텍스처로 간주됩니다. `src=` decal 또는 wall 테두리 이외의 MSS에서 이미지를 지정하는 속성.

렌더링할 때 텍스처는 를 일치시켜 오브젝트와 정렬됩니다. `anchor=` 개체의 질감 원점이 있는 질감 재료의 점(비네팅에서 작성).

<table id="table_992A6E93E4274B598A236F8F728F017A"> 
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
   <td colname="col3"> <p>없음. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>텍스처 해상도 </p> </td> 
   <td colname="col3"> <span class="codeph"> attribute::Resolution </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> 앵커= </span> </a> </p> </td> 
   <td colname="col2"> <p>텍스처 정렬 지점 </p> </td> 
   <td colname="col3"> <p>왼쪽 상단 모서리. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> repeat= </span> </a> </p> </td> 
   <td colname="col2"> <p>반복 모드 </p> </td> 
   <td colname="col3"> <p>0(직선 반복). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span> </a> </p> </td> 
   <td colname="col2"> <p>선명하게 하기 </p> </td> 
   <td colname="col3"> <p>0(선명하게 하기 없음). </p> </td> 
  </tr> 
 </tbody> 
</table>

이러한 기본 속성 외에도 반복 가능한 텍스처는 고급 응용 프로그램에 대해 다음과 같은 특수 목적 속성을 지원합니다.

<table id="table_A97365804CB143DEB31F26A65DA3CE04"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
   <th colname="col3" class="entry"> <p>기본값 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a" type="reference" format="dita" scope="local"> <span class="codeph"> grout= </span> </a> </p> </td> 
   <td colname="col2"> <p>그라우트 색상 및 두께, 세라믹 / 석재 타일 재료에 유용 </p> </td> 
   <td colname="col3"> <p>그룹에 이미 있음 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7" type="reference" format="dita" scope="local"> <span class="codeph"> 정렬= </span> </a> </p> </td> 
   <td colname="col2"> <p>정렬 모드(객체 간), 실내 장식용 어플리케이션에 사용 </p> </td> 
   <td colname="col3"> <p>가운데 일치 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rotate.md#reference-3745d74a913e4065b7ac009fb4fd9e3c" type="reference" format="dita" scope="local"> <span class="codeph"> rotate= </span> </a> </p> </td> 
   <td colname="col2"> <p>텍스처 회전 각도, 벽 오브젝트에서 지원되지 않음 </p> </td> 
   <td colname="col3"> <p>0(회전 없음) </p> </td> 
  </tr> 
 </tbody> 
</table>
