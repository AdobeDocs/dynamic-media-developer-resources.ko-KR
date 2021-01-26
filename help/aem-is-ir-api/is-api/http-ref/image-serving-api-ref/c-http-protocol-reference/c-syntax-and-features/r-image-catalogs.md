---
description: 이미지 카탈로그의 기능 및 구문은 이 섹션에 설명되어 있습니다.
seo-description: 이미지 카탈로그의 기능 및 구문은 이 섹션에 설명되어 있습니다.
seo-title: 이미지 카탈로그
solution: Experience Manager
title: 이미지 카탈로그
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d329807a-22b0-42a3-9297-8dad7a1dce43
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---


# 이미지 카탈로그{#image-catalogs}

이미지 카탈로그의 기능 및 구문은 이 섹션에 설명되어 있습니다.

이미지 카탈로그는 다음과 같은 기능을 제공합니다.

* 특정 메타데이터 및 수정자 명령을 사용하여 이미지를 지속적으로 연결할 수 있습니다.

   이미지 카탈로그의 항목은 단축키 표기법 `*`rootId/objId`*`을 사용하여 참조되며, 여기서 `*`rootId`*`는 이미지 카탈로그를 식별하고 `*`objId`*`는 카탈로그의 데이터 레코드를 식별합니다.
* JPEG 품질이나 워터마크를 적용할지 여부와 같은 특정 요청 속성의 기본값을 제공합니다.
* 글꼴, ICC 프로파일, 매크로 정의 및 요청 템플릿 관리

특정 이미지 카탈로그를 정의하지 않아도 기본 카탈로그( [!DNL default.ini])를 통해 이미지 카탈로그의 모든 기능을 사용할 수 있습니다.

요청의 URL 경로에 있는 `*`rootId`*`가 특정 이미지 카탈로그의 `attribute::RootId`과(와) 일치하는 경우 해당 카탈로그는 이 요청에 대한 기본 카탈로그가 됩니다. 기본 카탈로그는 전체 요청에 대한 기본 속성과 설정을 제공합니다. 일치하는 항목이 없으면 기본 카탈로그가 대신 사용됩니다.

`src=` 또는 `mask=` 명령에서 식별된 카탈로그는 현재 레이어에 다음과 같은 카탈로그 속성과 데이터를 제공합니다.

<table id="table_D3FA66EA5D054745900DE5A120885AA8"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 속성/데이터</b> </th> 
   <th class="entry"> <b> 주의</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 특성::DefaultExt</span> </p> </td> 
   <td> <p> 현재 레이어의 모든 이미지 파일 경로에 대한 기본 확장명 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 특성::만료</span> </p> </td> 
   <td> <p> 카탈로그 레코드가 없는 경우 <span class="codeph"> 카탈로그에 대한 기본값::만료</span> 또는 현재 레이어의 만료 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 속성::Icc*</span> </p> </td> 
   <td> <p> 요청 및/또는 현재 레이어에 대해 작업 중인 ICC 색상 프로필, 렌더링 의도 및 검은 점 보정 플래그 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 특성::RootPath</span> </p> </td> 
   <td> <p> 현재 레이어의 모든 소스 파일 경로에 사용됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 속성::Resolution</span> </p> </td> 
   <td> <p> <span class="codeph"> 카탈로그에 대한 기본값::Resolution</span>만 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 카탈로그::앵커</span> </p> </td> 
   <td> <p> 현재 레이어의 <span class="codeph"> 앵커=</span> 값에 대한 기본값 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 카탈로그::만료</span> </p> </td> 
   <td> <p> 모든 레이어의 최소 만료 값은 응답 이미지의 실시간 시간 값으로 사용됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 카탈로그::IccProfile</span> </p> </td> 
   <td> <p> 현재 레이어의 소스 이미지 색상 프로필 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 카탈로그::맵</span> </p> </td> 
   <td> <p> 현재 레이어의 이미지 맵 데이터 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 카탈로그::MaskPath</span> </p> </td> 
   <td> <p> 현재 레이어의 <span class="codeph"> mask=</span>에 대한 기본값 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 카탈로그::수정자</span> </p> </td> 
   <td> <p> 현재 레이어의 접두사 명령(같은 레이어에 대해 지정된 경우 <span class="codeph"> 카탈로그::Modifier</span>의 각 명령은 URL의 동일한 명령으로 재정의할 수 있음) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 카탈로그::경로</span> </p> </td> 
   <td> <p> 현재 레이어의 소스 이미지 파일 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 카탈로그::PostModifier</span> </p> </td> 
   <td> <p> 현재 레이어의 포스트픽스 명령(<span class="codeph"> 카탈로그::Modifier</span>과 유사하지만 <span class="codeph"> 카탈로그::PostModifier</span>의 명령은 URL 또는 <span class="codeph"> 카탈로그::Modifier</span>)에 지정된 동일한 명령을 재정의합니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 카탈로그::해상도</span> </p> </td> 
   <td> <p> 현재 레이어의 개체 해상도 </p> </td> 
  </tr> 
 </tbody> 
</table>

동일한 레이어 내에서 `src=` 및 `mask=`은 동일한 이미지 카탈로그(있는 경우)를 참조해야 합니다.

`icc=` 명령에 식별된 카탈로그는 카탈로그의 ICC 프로필 테이블에서 항목을 찾는 데만 사용됩니다. 다른 카탈로그 특성 또는 데이터는 포함되지 않습니다.

`*`rootId`*`가 카탈로그로 확인되고 `*`objId`*`가 이 카탈로그의 `catalog::Id`와 일치하면 `*`rootId/objId`*`가 다음과 같은 카탈로그 항목으로 효과적으로 대체됩니다.

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## 참조 {#section-00e4f6b39cd14244bcce537a3f831259}

[이미지 카탈로그 참조](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3),  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
