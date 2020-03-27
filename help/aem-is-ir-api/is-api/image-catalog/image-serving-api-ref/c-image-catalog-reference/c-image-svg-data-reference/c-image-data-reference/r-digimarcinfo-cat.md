---
description: Digimarc 이미지 정보. Digimarc 임베딩을 활성화하고 워터마크 유형과 이미지 관련 데이터를 지정합니다.
seo-description: Digimarc 이미지 정보. Digimarc 임베딩을 활성화하고 워터마크 유형과 이미지 관련 데이터를 지정합니다.
seo-title: DigimarcInfo
solution: Experience Manager
title: DigimarcInfo
topic: Scene7 Image Serving - Image Rendering API
uuid: 8371880e-47df-4333-b8a6-91feaf16c409
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# DigimarcInfo{#digimarcinfo}

Digimarc 이미지 정보. Digimarc 임베딩을 활성화하고 워터마크 유형과 이미지 관련 데이터를 지정합니다.

## 속성 {#section-62af219e8bac422b8541841221c9ce4f}

네 개의 정수 값을 쉼표로 구분합니다.

` *``*, *``*, *`typeflagsval1`*, *`val2`*`

` *`type`*` 은 Digimarc 임베딩을 활성화하고 워터마크 유형을 지정합니다.

<table id="table_3648951F14D94C5BAD097CFB783F1EE7"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> 유형</span></span> </p> </th> 
   <th class="entry"> <p><b>워터마크 유형</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>없음. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>기본. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>이미지 ID. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>거래 ID. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>저작권 년도입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

` *`flags`*` is a bit field with three values. 비트를 0으로 설정하면 복사 방지 컨텐츠를 나타내고, 비트는 제한된 컨텐츠를 나타내고, 비트는 2로 성인 컨텐츠를 나타냅니다.

<table id="table_00F218515FBE484F9D05CBAF14F9D045"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> 플래그</span></span> </p> </th> 
   <th class="entry"> <p><b>설명</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>- </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>복사 방지 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>제한됨. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>복사 방지, 제한적 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>성숙한 콘텐츠 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>5</b> </p> </td> 
   <td> <p>보호된 성인 컨텐츠 복사 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>6</b> </p> </td> 
   <td> <p>제한적, 성인 컨텐츠 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>7</b> </p> </td> 
   <td> <p>복사 방지, 제한적, 완성된 컨텐츠 </p> </td> 
  </tr> 
 </tbody> 
</table>

val1 ` *`및`*` val2의 ` *`해석은`*` 유형에 ` *`따라 다릅니다`*`.

<table id="table_6B29F76BC1974C12AB7124BF84B29EC2"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> 유형</span></span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val1 </span></span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val2 </span></span> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>사용되지 않습니다. </p> </td> 
   <td> <p>사용되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>사용되지 않습니다. </p> </td> 
   <td> <p>사용되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>이미지 ID. </p> </td> 
   <td> <p>사용되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>거래 ID. </p> </td> 
   <td> <p>사용되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>1년 </p> </td> 
   <td> <p>2년 저작권. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 기본값 {#section-4bb97e5f79074be89cc691e73449eb43}

필드가 없거나 비어 있는 경우 attribute::DigimarcInfo에서 상속됩니다.

## 예제 {#section-0f14727a0a2a408781c9df71fed7f42d}

&quot;0,0,0,0&quot;은 이 이미지에 대한 Digimarc 워터마크를 비활성화합니다.

&quot;1,5,0,0&quot;은 성인 및 복사 방지 컨텐츠 플래그가 설정된 기본 워터마크를 지정합니다.

&quot;2,0,4567,0&quot;은 이미지 ID가 있는 워터마크를 지정합니다.

&quot;3,2,56483,0&quot;은 거래 ID와 제한된 컨텐츠 플래그가 설정된 워터마크를 지정합니다.

&quot;4,0,1998,2001&quot;은 저작권 연수가 있는 워터마크를 지정합니다.

## 참조 {#section-4bd3e7272c5c4b8cb8c5ca1ac7ed1012}

[attribute::DigimarcInfo](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcinfo.md#reference-de88636cb9b4435a94e3d0a80f072667) , [attribute::DigimarcId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcid.md#reference-33e3eca7f1874510904e5c8645cecd68)
