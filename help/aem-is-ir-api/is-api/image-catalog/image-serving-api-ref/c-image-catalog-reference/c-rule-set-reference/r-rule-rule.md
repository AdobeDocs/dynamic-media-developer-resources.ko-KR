---
description: 요청 규칙 요소. <규칙 세트> 요소에서 하나 이상의 규칙은 선택 사항입니다.
solution: Experience Manager
title: 규칙
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4fabd469-c80c-422a-80b0-3d31ce191d58
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 6%

---

# 규칙{#rule}

요청 규칙 요소. `<ruleset>` 요소에서 하나 이상의 규칙은 선택 사항입니다.

## 속성 {#section-d4a3b0496c0c4aa5bd7da87203b9379b}

`OnMatch = "break" | "continue" | "error"`: 선택 사항입니다. 기본값은 &quot;break&quot;입니다.

`Replace = "first" | "all"`: 선택 사항입니다. 기본값은 &quot;first&quot;입니다.

`RequestType` =  *&quot; `types`&quot;*: 선택 사항입니다. 규칙이 적용되는 입력 컨텍스트를 지정합니다. *`types`* 는 쉼표로 구분된 목록이며, 다음 표에 나열된 토큰 중 하나 이상을 포함할 수 있습니다. `RequestType`을 지정하지 않으면 지원되는 모든 컨텍스트에서 수신되는 요청에 규칙이 적용됩니다.

<table id="table_4935E1ED03624DA6AF3F8DC9AAA10237"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><b>토큰</b> </p> </th> 
   <th class="entry"> <p><b>컨텍스트</b> </p> </th> 
   <th class="entry"> <p><b>설명</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> is</span> </p> </td> 
   <td> <p> <span class="filepath"> /is/image/</span> </p> </td> 
   <td> <p>이미지 제공 요청에 적용됨 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> ir</span> </p> </td> 
   <td> <p> <span class="filepath"> /ir/render/</span> </p> </td> 
   <td> <p>이미지 렌더링 요청에 적용됨 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 정적</span> </p> </td> 
   <td> <p> <span class="filepath"> /is/content/</span> </p> </td> 
   <td> <p>정적 콘텐츠 요청에 적용됨 </p> </td> 
  </tr> 
 </tbody> 
</table>

**`Name = "text"`**: 선택 사항입니다. 디버그 로그 및 오류 메시지에서 `<rule>` 요소를 식별하는 데 사용됩니다.

`  *`속성`* ="value"`: 선택 사항입니다. `<rule>` 요소는 모든 조합에서 다음 속성 중 하나를 정의할 수 있습니다. 지정되고 규칙이 성공적으로 일치하면 이 요청에 대한 해당 카탈로그 속성을 재정의합니다. 기본값은 `RequestType="is"`입니다.

<table id="table_67AED5BEADDF4DAC99B5EF46438C1ABC"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <span class="varname"> 속성  </span> </b> </th> 
   <th class="entry"> <p>해당 이미지 카탈로그 속성 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> DefaultImageMode</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782" type="reference" format="dita" scope="local"> attribute::DefaultImageMode</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> ErrorImage</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c" type="reference" format="dita" scope="local"> attribute::ErrorImage</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 만료</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7" type="reference" format="dita" scope="local"> 속성::만료</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> MaxPix</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5" type="reference" format="dita" scope="local"> 속성::MaxPix  </a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RequestLock</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0" type="reference" format="dita" scope="local"> attribute::RequestLock</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RequestObfusation</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd" type="reference" format="dita" scope="local"> attribute::RequestObfusation</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RootUrl</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rooturl.md#reference-3b0e43881020409cbe642366913cf137" type="reference" format="dita" scope="local"> attribute::RootUrl</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> SavePath</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-savepath.md#reference-9c4686dc153b41d8a0751cde83615432" type="reference" format="dita" scope="local"> 속성::SavePath</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 워터마크</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b" type="reference" format="dita" scope="local"> attribute::WaterMark</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

자세한 내용은 해당 이미지 카탈로그 속성의 설명을 참조하십시오.

만료 속성은 기본 속성 값만 덮어씁니다. 특정 `catalog::Expiration` 값이 요청에 적용되는 경우 무시가 무시됩니다.

## 데이터 {#section-8fce013a4c724da58af3fee4e7a90e72}

<table id="simpletable_4F1C03671DA942A3A332B2C686A63C52"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;expression&gt;</span> </p></td> 
  <td class="stentry"> <p>선택 사항입니다 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;substitution&gt;</span> </p></td> 
  <td class="stentry"> <p>선택 사항입니다 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;addressfilter&gt;</span> </p></td> 
  <td class="stentry"> <p>선택 사항입니다 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;헤더&gt;</span> </p></td> 
  <td class="stentry"> <p>선택 사항입니다 </p></td> 
 </tr> 
</table>

## 주의 {#section-0c5fbc363070419d8c9800b0c02dc9f9}

`<expression>` 및 `<substitution>` 둘 다 지정되고 캡처된 하위 문자열을 사용하지 않으면 일치하는 첫 번째 하위 문자열은 `<substitution>`로 바뀝니다.

`<expression>`을 지정하지 않으면 경로가 일치하고 `<substitution>`이 경로 끝에 추가됩니다.

`<substitution>`을 지정하지 않으면 경로나 쿼리 변환이 발생하지 않지만 지정된 카탈로그 특성이 무시됩니다. `<substitution>`이 비어 있으면 일치하는 하위 문자열이 제거됩니다.

`<addressfilter>`은 일치가 발생했을 때, 쿼리 규칙이 적용되기 전에만 적용됩니다.
