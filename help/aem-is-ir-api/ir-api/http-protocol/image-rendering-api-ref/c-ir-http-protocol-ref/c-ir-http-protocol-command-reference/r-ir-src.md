---
description: 자료 파일. 단일 자료 카탈로그 참조 형식으로 또는 쉼표로 구분된 하나 또는 두 개의 이미지 또는 자료 데이터 파일로 재료 데이터를 지정합니다.
solution: Experience Manager
title: src
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: aff45f0f-e672-40da-9cc8-db83cf3922ff
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 2%

---

# src{#src}

자료 파일. 단일 자료 카탈로그 참조 형식으로 또는 쉼표로 구분된 하나 또는 두 개의 이미지 또는 자료 데이터 파일로 재료 데이터를 지정합니다.

`src = *``*|{{ *``*| *``*}[, *`catalogEntrymaterialFileembeddedReqmaterialFile`*]`

`srcE= *`name`*`

`srcN= *`색인`*`

<table id="simpletable_A64C4F084C0A4DDCA45A921D4BD7AAEA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catalogEntry</span> </p></td> 
  <td class="stentry"> <p><span class="codeph">[/][<span class="varname"> catId</span>/]<span class="varname"> recId</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> materialFile</span> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> styleFile</span>|<span class="varname"> imageFile</span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> embeddedReq</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">&amp;lbrase;'is&amp;lbrase;'<span class="varname"> isReq</span>'&amp;rbrase;'&amp;rbrase;|&amp;lbrase;'ir&amp;rbrase;'<span class="varname"> irReq</span>'&amp;rbrasce;'|&amp;lbrase;'&amp;<span class="varname"> foreignReq</span>'&amp;rbrases;'</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p></td> 
  <td class="stentry"> <p>재료 카탈로그 ID(<span class="codeph"> 특성::RootId</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>재료 카탈로그 항목(<span class="codeph"> 카탈로그::Id</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> styleFile</span> </p></td> 
  <td class="stentry"> <p>재료 스타일 파일(<span class="filepath"> .vnc</span> 또는 <span class="filepath"> .vnw</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> imageFile</span> </p></td> 
  <td class="stentry"> <p>이미지 데이터 파일입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> isReq</span> </p></td> 
  <td class="stentry"> <p>이미지 제공 요청. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> irReq</span> </p></td> 
  <td class="stentry"> <p>이미지 렌더링에 대한 요청. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> foreignReq</span> </p></td> 
  <td class="stentry"> <p>외부 서버에 요청합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> name</span> </p></td> 
  <td class="stentry"> <p>포함된 재료의 이름입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 색인</span> </p></td> 
  <td class="stentry"> <p>포함된 재료의 0 기반 인덱스 번호입니다. </p></td> 
 </tr> 
</table>

반복 가능한 텍스쳐, 전사 및 월페이퍼 재료는 하나의 이미지가 필요합니다. 이 이미지는 파일 또는 임베디드 요청으로 지정될 수 있습니다.

캐비닛 자료에 캐비닛 스타일 파일( [!DNL .vnc])이 있어야 하며 중첩 요청으로 지정할 수 없습니다. 텍스처 이미지 파일은 캐비닛의 경우 선택 사항이며, 지정한 경우 파일 또는 포함된 요청일 수 있습니다.

Window Covering 자료에 필요한 Window Covering 스타일 파일( [!DNL .vnw])은 중첩 요청으로 지정할 수 없습니다. 텍스처 파일은 선택 사항이며, 지정되는 경우 파일 또는 포함된 요청일 수 있습니다.

이미지 렌더링에서는 자료 카탈로그, 카탈로그 항목 및 데이터 파일을 조회하기 위해 이미지 제공 장치와 동일한 규칙을 사용합니다. 자세한 내용은 이미지 제공 설명서의 *`object`* 데이터 유형 설명을 참조하십시오.

*`materialFile`* 은 을(를) 기준으로 하는 경로입니다 `attribute::RootPath`.

*`foreignReq`* 는 을 기준으로 하는 URL이거나  `attribute::RootUrl`을 설정한 경우 절대 URL일 수  `attribute::AllowDirectUrls` 있습니다.

*`catId`*&#x200B;을 지정하지 않으면 세션 카탈로그가 사용됩니다.

`srcE=` 및  `srcN=` 는 비네트에 포함된 자료에 대한 액세스를 제공합니다.

## 지원되는 파일 형식 {#section-f2186d3eef834fc8bbecb2bc68daacad}

이미지 렌더링은 Dynamic Media 이미지 제공 기능과 동일한 소스 이미지 형식을 지원합니다.

여러 해상도의 이미지 데이터가 필요한 응용 프로그램은 Scene7 피라미드 TIFF(PTIFF) 다중 해상도 형식을 사용할 때 가장 잘 수행됩니다. 이미지 제공 기능에는 지원되는 모든 포맷에서 PTIFF 이미지를 생성하는 IC(Image Converter) 유틸리티가 포함되어 있습니다.

지원되는 파일 형식의 전체 목록은 이미지 제공 설명서의 IC 유틸리티에 대한 설명을 참조하십시오.

## 속성 {#section-e68d03788d534e2184147987d51dfd0f}

재료 속성입니다. 단색을 제외한 모든 재료에 필요합니다(단색 재료에는 허용되지 않음). 모든 문자열은 대/소문자를 구분합니다. *`index`* 0보다 커야 합니다.

## 기본값 {#section-dde549c1917540dc8f9555962202da3c}

없음.

## 예 {#section-675865444f8a4d35b9fc6e58b36e3438}

별도의 반복 가능한 텍스처가 있는 컬러 캐비닛의 MSS:

`…&obj=cabinets&src=cabs/maple02.vnc,cabs/maple.jpg&res=40&color=185,105,35&…`

&#39; `12-3-2`&#39; 레코드의 자료 카탈로그 `'cat`&#39;에 동일한 자료를 찾을 수 있습니다.

`…&obj=cabinets&src=cat/12-3-2&…`

텍스처 이미지를 가져오도록 이미지 제공 서비스에 대한 중첩 요청:

`…&obj=main&src=is{texCatalog/texture123?res=30}&res=30&…`

## 참조 {#section-d01d25b8903e4f5ca6aef4a084fca6b7}

[재료 카탈로그](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2),  [속성::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402),  [속성::AllowDirectUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-allowdirecturls.md#reference-02000c0f3c494292bad8425d06268882)
