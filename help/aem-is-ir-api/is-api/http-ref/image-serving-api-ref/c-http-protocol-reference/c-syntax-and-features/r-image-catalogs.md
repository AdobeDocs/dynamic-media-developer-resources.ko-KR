---
description: 이미지 카탈로그의 기능과 구문은 이 섹션에 설명되어 있습니다.
solution: Experience Manager
title: 이미지 카탈로그
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c83ad2-a932-4df2-92ff-ab34d4a5b1a7
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 0%

---

# 이미지 카탈로그{#image-catalogs}

이미지 카탈로그의 기능과 구문은 이 섹션에 설명되어 있습니다.

이미지 카탈로그는 다음 기능을 제공합니다.

* 특정 메타데이터 및 수정자 명령과 이미지를 영구적으로 연결할 수 있습니다.

   이미지 카탈로그의 항목은 바로 가기 표기법을 사용하여 참조됩니다 `*`rootId/objId`*`, 위치 `*`rootId`*` 이미지 카탈로그를 식별하고 `*`objId`*` 카탈로그에서 데이터 레코드를 식별합니다.
* JPEG 품질 또는 워터마크 적용 여부와 같은 특정 요청 속성의 기본값을 제공합니다.
* 글꼴, ICC 프로필, 매크로 정의 및 요청 템플릿 관리

특정 이미지 카탈로그를 정의하지 않더라도 기본 카탈로그( [!DNL default.ini]).

If `*`rootId`*` 요청의 URL 경로에서 과 일치합니다 `attribute::RootId` 특정 이미지 카탈로그의 기본 카탈로그가 이 요청의 기본 카탈로그가 됩니다. 기본 카탈로그는 전체 요청에 대한 기본 속성 및 설정을 제공합니다. 일치하는 항목이 없으면 기본 카탈로그가 대신 사용됩니다.

에서 식별된 카탈로그 `src=` 또는 `mask=` 명령은 현재 레이어에 다음과 같은 카탈로그 속성 및 데이터를 제공합니다.

<table id="table_D3FA66EA5D054745900DE5A120885AA8"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 속성/데이터</b> </th> 
   <th class="entry"> <b> 주의</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::DefaultExt</span> </p> </td> 
   <td> <p> 현재 레이어의 모든 이미지 파일 경로에 대한 기본 확장입니다 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 속성::만료</span> </p> </td> 
   <td> <p> 기본값 <span class="codeph"> 카탈로그::만료</span> 카탈로그 레코드가 없는 경우 현재 레이어의 만료 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 특성::Icc*</span> </p> </td> 
   <td> <p> 작업 중인 ICC 색상 프로파일, 렌더링 의도 및/또는 현재 레이어에 대한 블랙포인트 보상 플래그 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootPath</span> </p> </td> 
   <td> <p> 현재 레이어의 모든 소스 파일 경로에 사용됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::resolution</span> </p> </td> 
   <td> <p> 기본값 <span class="codeph"> 카탈로그::해상도</span> 전용 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 카탈로그::앵커</span> </p> </td> 
   <td> <p> 기본값은 입니다. <span class="codeph"> 앵커=</span> 현재 레이어의 값 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 카탈로그::만료</span> </p> </td> 
   <td> <p> 모든 레이어의 가장 작은 만료 값이 회신 이미지의 실시간 만료 값으로 사용됩니다 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 카탈로그::IccProfile</span> </p> </td> 
   <td> <p> 현재 레이어의 소스 이미지 색상 프로파일 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 카탈로그::맵</span> </p> </td> 
   <td> <p> 현재 레이어의 이미지 맵 데이터 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 카탈로그::MaskPath</span> </p> </td> 
   <td> <p> 기본값 <span class="codeph"> 마스크=</span> 현재 레이어의 경우 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 카탈로그::수정자</span> </p> </td> 
   <td> <p> 현재 레이어의 접두사 명령(각 명령 <span class="codeph"> 카탈로그::수정자</span> 동일한 레이어에 대해 지정된 경우 URL에서 동일한 명령으로 대체할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 카탈로그::경로</span> </p> </td> 
   <td> <p> 현재 레이어의 소스 이미지 파일 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 카탈로그::PostModifier</span> </p> </td> 
   <td> <p> 현재 레이어의 포스트픽스 명령(다음과 유사) <span class="codeph"> 카탈로그::수정자</span>의 <span class="codeph"> 카탈로그::PostModifier</span> url 또는 <span class="codeph"> 카탈로그::수정자</span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 카탈로그::해상도</span> </p> </td> 
   <td> <p> 현재 레이어의 개체 해상도 </p> </td> 
  </tr> 
 </tbody> 
</table>

같은 레이어 내에서 `src=` 및 `mask=` 동일한 이미지 카탈로그를 참조해야 합니다(있는 경우).

에서 식별된 카탈로그 `icc=` 명령은 카탈로그의 ICC 프로파일 테이블에서 항목을 찾는 데만 사용됩니다. 다른 카탈로그 속성이나 데이터가 포함되어 있지 않습니다.

if, `*`rootId`*` 카탈로그로 확인되고 `*`objId`*` 와 일치함 `catalog::Id` 이 카탈로그에서 `*`rootId/objId`*` 은 다음과 같은 카탈로그 항목으로 효과적으로 대체됩니다.

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## 참조 {#section-00e4f6b39cd14244bcce537a3f831259}

[이미지 카탈로그 참조](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [마스크=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [앵커=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
