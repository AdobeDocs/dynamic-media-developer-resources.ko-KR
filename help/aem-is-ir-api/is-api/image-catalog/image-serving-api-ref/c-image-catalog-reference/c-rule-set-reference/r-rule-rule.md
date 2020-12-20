---
description: 요청 규칙 요소를 참조하십시오. <규칙 세트> 요소에서 하나 이상의 규칙이 선택 사항입니다.
seo-description: 요청 규칙 요소를 참조하십시오. <규칙 세트> 요소에서 하나 이상의 규칙이 선택 사항입니다.
seo-title: 규칙
solution: Experience Manager
title: 규칙
topic: Scene7 Image Serving - Image Rendering API
uuid: 8b8e5b06-a0b7-47e1-942d-0297d08c313b
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 6%

---


# 규칙{#rule}

요청 규칙 요소를 참조하십시오. 하나 이상의 규칙은 `<ruleset>` 요소에서 선택 사항입니다.

## 속성 {#section-d4a3b0496c0c4aa5bd7da87203b9379b}

`OnMatch = "break" | "continue" | "error"`: 선택 사항입니다. 기본값은 &quot;break&quot;입니다.

`Replace = "first" | "all"`: 선택 사항입니다. 기본값은 &quot;first&quot;입니다.

`RequestType` =  *&quot;`types`&quot;*:선택 사항. 규칙이 적용되는 입력 컨텍스트를 지정합니다. *`types`* 은 쉼표로 구분된 목록으로, 다음 표에 나열된 토큰 중 하나 이상을 포함할 수 있습니다. `RequestType`을(를) 지정하지 않으면 지원되는 모든 컨텍스트에서 수신되는 요청에 규칙이 적용됩니다.

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

**`Name = "text"`**: 선택 사항입니다. 디버그 로그 및 오류 메시지에서 `<rule>` 요소를 식별하는 데 사용됩니다.

`  *`속성`* ="value"`:선택 사항. `<rule>` 요소는 조합에서 다음 속성을 정의할 수 있습니다. 지정된 경우 규칙이 성공적으로 일치하면 이 요청에 해당하는 카탈로그 특성을 재정의합니다. 기본값은 `RequestType="is"`입니다.

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
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782" type="reference" format="dita" scope="local"> 특성::DefaultImageMode</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> ErrorImage</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c" type="reference" format="dita" scope="local"> 특성::ErrorImage</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 만료</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7" type="reference" format="dita" scope="local"> 특성::만료</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> MaxPix</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5" type="reference" format="dita" scope="local"> 특성::MaxPix  </a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RequestLock</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0" type="reference" format="dita" scope="local"> 특성::RequestLock</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RequestObfuscation</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd" type="reference" format="dita" scope="local"> 특성::RequestObfuscation</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 루트 URL</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rooturl.md#reference-3b0e43881020409cbe642366913cf137" type="reference" format="dita" scope="local"> 특성::RootUrl</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> SavePath</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-savepath.md#reference-9c4686dc153b41d8a0751cde83615432" type="reference" format="dita" scope="local"> 속성::SavePath</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> WaterMark</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b" type="reference" format="dita" scope="local"> 특성::WaterMark</a> </p> </td> 
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

`<expression>` 및 `<substitution>`이 모두 지정되고 캡처된 하위 문자열이 사용되지 않으면 첫 번째 일치 하위 문자열이 `<substitution>`로 대체됩니다.

`<expression>`이(가) 지정되지 않으면 모든 경로가 일치하고 `<substitution>`이 경로의 끝에 추가됩니다.

`<substitution>`이(가) 지정되지 않은 경우 경로 또는 쿼리 변환이 발생하지 않지만 지정된 카탈로그 속성은 재정의됩니다. `<substitution>`이(가) 비어 있으면 일치하는 하위 문자열이 제거됩니다.

`<addressfilter>`은 일치 작업이 발생할 때와 쿼리 규칙이 적용되기 전에만 적용됩니다.
