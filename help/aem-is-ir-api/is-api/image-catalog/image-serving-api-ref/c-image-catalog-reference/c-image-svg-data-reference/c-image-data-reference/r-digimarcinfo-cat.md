---
title: DigimarcInfo
description: Digimarc 이미지 정보입니다. Digimarc 포함 기능을 활성화하고 워터마크 유형 및 관련 이미지 관련 데이터를 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 87f4d8f0-02b9-4511-9151-89c58116c78d
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 13%

---

# DigimarcInfo{#digimarcinfo}

Digimarc 이미지 정보입니다. Digimarc 포함 기능을 활성화하고 워터마크 유형 및 관련 이미지 관련 데이터를 지정합니다.

## 속성 {#section-62af219e8bac422b8541841221c9ce4f}

네 개의 정수 값으로, 쉼표로 구분됩니다.

`*`유형`*, *`플래그`*, *`val1`*, *`val2`*`

`*`유형`*` Digimarc 포함 기능을 활성화하고 워터마크 유형을 지정합니다.

<table id="table_3648951F14D94C5BAD097CFB783F1EE7"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> 유형</span> </span> </p> </th> 
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
   <td> <p>저작권 연도별. </p> </td> 
  </tr> 
 </tbody> 
</table>

`*`플래그`*` 는 세 개의 값이 있는 비트 필드입니다. 복사 방지 컨텐츠를 나타내려면 비트 0을 설정하고, 제한된 컨텐츠를 나타내려면 비트 1을 설정하고, 성인 컨텐츠를 나타내려면 비트 2를 설정합니다.

<table id="table_00F218515FBE484F9D05CBAF14F9D045"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> 플래그</span> </span> </p> </th> 
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
   <td> <p>복사 방지. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2개</b> </p> </td> 
   <td> <p>제한됨. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>복사 금지, 제한. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>성숙한 컨텐츠. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>5</b> </p> </td> 
   <td> <p>보호된 성인 컨텐츠 복사 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>6</b> </p> </td> 
   <td> <p>제한, 성인용 콘텐츠. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>7</b> </p> </td> 
   <td> <p>복사, 보호, 제한, 완성 컨텐츠 </p> </td> 
  </tr> 
 </tbody> 
</table>

해석 `*`val1`*` 및 `*`val2`*` 다음 사항에 따라 `*`유형`*`:

<table id="table_6B29F76BC1974C12AB7124BF84B29EC2"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> 유형</span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val1 </span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val2 </span> </span> </p> </th> 
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
   <td> <p><b>2개</b> </p> </td> 
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
   <td> <p>첫 저작권 연도. </p> </td> 
   <td> <p>2차 저작권 연도. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 기본값 {#section-4bb97e5f79074be89cc691e73449eb43}

다음 속성에서 상속됨::DigimarcInfo는 필드가 없거나 비어 있는 경우에 상속됩니다.

## 예제 {#section-0f14727a0a2a408781c9df71fed7f42d}

&quot;0,0,0,0&quot;은 이 이미지에 대한 Digimarc 워터마킹을 사용하지 않습니다.

&quot;1,5,0,0&quot;은(는) 성체 및 복사 방지 컨텐츠 플래그가 설정된 기본 워터마크를 지정합니다.

&quot;2,0,4567,0&quot;은 이미지 ID가 있는 워터마크를 지정합니다.

&quot;3,2,56483,0&quot;은 트랜잭션 ID와 제한된 컨텐츠 플래그가 설정된 워터마크를 지정합니다.

&quot;4,0,198,2001&quot;은 저작권 연수가 있는 워터마크를 지정합니다.

## 참조 {#section-4bd3e7272c5c4b8cb8c5ca1ac7ed1012}

[attribute::DigimarcInfo](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcinfo.md#reference-de88636cb9b4435a94e3d0a80f072667) , [특성::DigimarcId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcid.md#reference-33e3eca7f1874510904e5c8645cecd68)
