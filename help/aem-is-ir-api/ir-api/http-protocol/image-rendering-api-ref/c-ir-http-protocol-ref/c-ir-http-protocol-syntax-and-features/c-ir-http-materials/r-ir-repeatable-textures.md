---
description: 반복 가능한 텍스처에는 직물(의류 및 업홀스터리 모두), 담벼락 바닥 커버, 벽면 커버링, 벽면 재질, 카운터톱 재질, 나무 그레인 텍스처, 지붕 및 측판 재질, 기타 일반적인 텍스처와 같은 실내 및 외부 재질이 포함됩니다.
solution: Experience Manager
title: 반복 가능한 텍스처
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 3%

---


# 반복 가능한 텍스처{#repeatable-textures}

반복 가능한 텍스처에는 직물(의류 및 업홀스터리 모두), 담벼락 바닥 커버, 벽면 커버링, 벽면 재질, 카운터톱 재질, 나무 그레인 텍스처, 지붕 및 측판 재질, 기타 일반적인 텍스처와 같은 실내 및 외부 재질이 포함됩니다.

반복 가능한 텍스처는 플랫, 플로우, 스케치, 평면, 벽 및 캐비닛 객체에 적용할 수 있습니다. 텍스트가 아닌 개체에 적용할 경우 개체는 `color=`(또는 `color=`가 지정되지 않은 경우 `bgc=`)으로 페인팅됩니다.

이미지를 지정하는 `src=` 특성이 있고, 일반 또는 벽 테두리가 아닌 MSS에서 발생하는 경우 해당 재질은 텍스처로 간주됩니다.

렌더링할 때 텍스처는 텍스처 재질의 `anchor=` 점과 비네팅에서 작성되는 대로 개체의 텍스처 원점을 일치시켜 개체에 맞춰 정렬됩니다.

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>반복 가능한 텍스처 이미지;required </p> </td> 
   <td colname="col3"> <p>없음. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res=  </span> </a> </p> </td> 
   <td colname="col2"> <p>텍스처 해상도 </p> </td> 
   <td colname="col3"> <span class="codeph"> 속성::Resolution  </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> anchor=  </span> </a> </p> </td> 
   <td colname="col2"> <p>텍스처 정렬 점 </p> </td> 
   <td colname="col3"> <p>왼쪽 위 모서리 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> 반복=  </span> </a> </p> </td> 
   <td colname="col2"> <p>반복 모드 </p> </td> 
   <td colname="col3"> <p>0(연속 반복). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp=  </span> </a> </p> </td> 
   <td colname="col2"> <p>선명하게 하기 </p> </td> 
   <td colname="col3"> <p>0(선명하게 하지 않음). </p> </td> 
  </tr> 
 </tbody> 
</table>

반복 가능한 텍스처는 이러한 기본 속성 외에도 고급 응용 프로그램에 대해 다음과 같은 특수 목적 속성을 지원합니다.

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a" type="reference" format="dita" scope="local"> <span class="codeph"> grout=  </span> </a> </p> </td> 
   <td colname="col2"> <p>그라우트 색상 및 두께세라믹/돌 타일 재질 </p> </td> 
   <td colname="col3"> <p>이미지가 이미 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7" type="reference" format="dita" scope="local"> <span class="codeph"> 정렬=  </span> </a> </p> </td> 
   <td colname="col2"> <p>정렬 모드(객체 간);유지 관리 응용 프로그램에 사용됨 </p> </td> 
   <td colname="col3"> <p>가운데 일치 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rotate.md#reference-3745d74a913e4065b7ac009fb4fd9e3c" type="reference" format="dita" scope="local"> <span class="codeph"> rotate= </span> </a> </p> </td> 
   <td colname="col2"> <p>텍스처 회전 각도;벽 객체에서 지원되지 않음 </p> </td> 
   <td colname="col3"> <p>0(회전 없음) </p> </td> 
  </tr> 
 </tbody> 
</table>

