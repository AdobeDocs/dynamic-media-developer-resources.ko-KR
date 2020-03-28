---
description: 요청 규칙 요소를 참조하십시오. <ruleset> 요소에서 하나 이상의 규칙이 선택 사항입니다.
seo-description: 요청 규칙 요소를 참조하십시오. <ruleset> 요소에서 하나 이상의 규칙이 선택 사항입니다.
seo-title: 규칙
solution: Experience Manager
title: 규칙
topic: Scene7 Image Serving - Image Rendering API
uuid: 8b8e5b06-a0b7-47e1-942d-0297d08c313b
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# 규칙{#rule}

요청 규칙 요소를 참조하십시오. 요소에서는 하나 이상의 규칙이 선택 `<ruleset>` 사항입니다.

## 속성 {#section-d4a3b0496c0c4aa5bd7da87203b9379b}

`OnMatch = "break" | "continue" | "error"`: 선택 사항입니다. 기본값은 &quot;break&quot;입니다.

`Replace = "first" | "all"`: 선택 사항입니다. 기본값은 &quot;first&quot;입니다.

`RequestType` = *&quot;`types`&quot;*:선택 사항입니다. 규칙이 적용되는 입력 컨텍스트를 지정합니다. *`types`* 은 쉼표로 구분된 목록으로, 다음 표에 나열된 토큰 중 하나 이상을 포함할 수 있습니다. 을 지정하지 `RequestType` 않으면 지원되는 모든 컨텍스트에서 수신된 요청에 규칙이 적용됩니다.

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
   <td> <p>이미지 제공 요청에 적용 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> ir</span> </p> </td> 
   <td> <p> <span class="filepath"> /ir/render/</span> </p> </td> 
   <td> <p>이미지 렌더링 요청에 적용 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 정적</span> </p> </td> 
   <td> <p> <span class="filepath"> /is/content/</span> </p> </td> 
   <td> <p>정적 컨텐츠 요청에 적용 </p> </td> 
  </tr> 
 </tbody> 
</table>

**`Name = "text"`**: 선택 사항입니다. 디버그 로그 및 오류 메시지의 `<rule>` 요소를 식별하는 데 사용됩니다.

`  *`속성`* ="value"`:선택 사항입니다. `<rule>` 요소에서는 조합에서 다음 속성을 정의할 수 있습니다. 지정된 경우 규칙이 성공적으로 일치하면 이 요청에 대해 해당 카탈로그 특성을 덮어씁니다. Default is `RequestType="is"`.

<table id="table_67AED5BEADDF4DAC99B5EF46438C1ABC"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 속성 <span class="varname"></span></b> </th> 
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
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c" type="reference" format="dita" scope="local"> 속성::ErrorImage</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 만료</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7" type="reference" format="dita" scope="local"> 속성::만료</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> MaxPix</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5" type="reference" format="dita" scope="local"> 속성::MaxPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RequestLock</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0" type="reference" format="dita" scope="local"> 속성::RequestLock</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RequestObfuscation</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd" type="reference" format="dita" scope="local"> 속성::RequestObfuscation</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RootUrl</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rooturl.md#reference-3b0e43881020409cbe642366913cf137" type="reference" format="dita" scope="local"> 속성::RootUrl</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> SavePath</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-savepath.md#reference-9c4686dc153b41d8a0751cde83615432" type="reference" format="dita" scope="local"> 속성::SavePath</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 워터마크</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b" type="reference" format="dita" scope="local"> 속성::WaterMark</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

자세한 내용은 해당 이미지 카탈로그 속성의 설명을 참조하십시오.

만료 속성은 기본 속성 값만 덮어씁니다. 특정 `catalog::Expiration` 값이 요청에 적용되는 경우 재정의가 무시됩니다.

## 데이터 {#section-8fce013a4c724da58af3fee4e7a90e72}

<table id="simpletable_4F1C03671DA942A3A332B2C686A63C52"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;expression&gt;</span> </p></td> 
  <td class="stentry"> <p>선택 사항입니다 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;대체&gt;</span> </p></td> 
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

및 를 모두 `<expression>` 지정하고 캡처된 하위 문자열을 사용하지 않으면 첫 번째 일치하는 하위 문자열이 로 대체됩니다 `<substitution>` `<substitution>`.

을 지정하지 `<expression>` `<substitution>` 않으면 모든 경로가 일치하고 경로 끝에 추가됩니다.

지정하지 `<substitution>` 않으면 경로 또는 쿼리 변환이 발생하지 않지만 지정된 카탈로그 속성은 무시됩니다. 비어 `<substitution>` 있으면 일치하는 하위 문자열이 제거됩니다.

는 `<addressfilter>` 일치 항목이 발생할 때와 쿼리 규칙이 적용되기 전에만 적용됩니다.
