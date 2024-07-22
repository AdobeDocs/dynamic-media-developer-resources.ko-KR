---
description: 규칙 요소를 요청합니다. <ruleset> 요소에서 하나 이상이 선택 사항입니다.
solution: Experience Manager
title: 규칙
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8f56012c-d01c-489c-9d18-91e256f72012
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 3%

---

# 규칙{#rule}

규칙 요소를 요청합니다. `<ruleset>` 요소에서 하나 이상이 선택 사항입니다.

## 속성 {#section-aa23349645434db99d46957a96f2e1e1}

`OnMatch="break"|"continue"|"error"`은(는) 선택 사항입니다. 기본값은 &quot;break&quot;입니다.

` Name=" *`text`*"` 선택 사항입니다. 디버그 로그 및 오류 메시지에서 `<rule>` 요소를 식별하는 데 사용됩니다.

또한 `<rule>` 요소는 임의의 조합으로 다음 특성을 정의할 수 있습니다. 지정되고 규칙이 성공적으로 일치하면 이 요청에 대한 해당 카탈로그 속성이 재정의됩니다.

<table id="table_AFEFDE61C9ED40019C10D8FE5B16CA23"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>&lt;rule&gt; 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>해당 이미지 카탈로그 속성 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> DefaultPix </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f" type="reference" format="dita" scope="local"> 특성::DefaultPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ErrorImage </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0" type="reference" format="dita" scope="local"> 특성::ErrorImage </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 만료 </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996" type="reference" format="dita" scope="local"> 특성::만료 </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MaxPix </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657" type="reference" format="dita" scope="local"> 특성::MaxPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RootUrl </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402" type="reference" format="dita" scope="local"> 특성::RootUrl </a> </p> </td> 
  </tr> 
 </tbody> 
</table>

자세한 내용은 해당 이미지 카탈로그 속성의 설명을 참조하십시오.

만료 특성은 기본 특성 값만 재정의합니다. 특정 `catalog::Expiration` 값이 요청에 적용되는 경우 무시됩니다.

## 데이터 {#section-401b6dfce082490f81229a19b73f2562}

<table id="simpletable_A7E17B52AF754687ACCFFBE747939331"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;표현식&gt; </span> </p> </td> 
  <td class="stentry"> <p>선택적. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;대체&gt; </span> </p> </td> 
  <td class="stentry"> <p>선택적. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;addressfilter&gt; </span> </p> </td> 
  <td class="stentry"> <p>선택적. </p> </td> 
 </tr> 
</table>

## 주의 {#section-a27b91f9a03047c0bb7edc0967fb4216}

`<expression>`과(와) `<substitution>`을(를) 모두 지정하고 캡처된 하위 문자열을 사용하지 않으면 일치하는 첫 번째 하위 문자열이 `<substitution>`(으)로 바뀝니다.

`<expression>`을(를) 지정하지 않으면 일치하는 경로가 있으며 `<substitution>`이(가) 경로 끝에 추가됩니다.

`<substitution>`을(를) 지정하지 않으면 일치하는 하위 문자열이 제거됩니다.

`<addressfilter>`은(는) 일치가 발생하는 경우에만 쿼리 규칙이 적용되기 전에 적용됩니다.
