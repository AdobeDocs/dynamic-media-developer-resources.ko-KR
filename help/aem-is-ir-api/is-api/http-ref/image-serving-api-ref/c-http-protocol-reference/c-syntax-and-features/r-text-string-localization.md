---
description: 텍스트 문자열 현지화를 통해 이미지 카탈로그에는 동일한 문자열 값에 대한 여러 로케일별 표현이 포함될 수 있습니다.
seo-description: 텍스트 문자열 현지화를 통해 이미지 카탈로그에는 동일한 문자열 값에 대한 여러 로케일별 표현이 포함될 수 있습니다.
seo-title: 텍스트 문자열 현지화
solution: Experience Manager
title: 텍스트 문자열 현지화
topic: Scene7 Image Serving - Image Rendering API
uuid: bdff2403-e3bb-4b3f-a8d7-bb108c1fbee8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 텍스트 문자열 현지화{#text-string-localization}

텍스트 문자열 현지화를 통해 이미지 카탈로그에는 동일한 문자열 값에 대한 여러 로케일별 표현이 포함될 수 있습니다.

서버는 클라이언트와 함께 지정된 로케일과 일치하는 표현을 클라이언트로 반환하므로 클라이언트측 로컬라이제이션을 `locale=`방지하고 IS 텍스트 요청과 함께 적절한 `locale=` 값을 전송하여 응용 프로그램이 로케일을 전환할 수 있습니다.

## 범위 {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

텍스트 문자열 현지화는 다음 카탈로그 필드에 현지화 토큰 ` ^loc= *`locId를`*^` 포함하는 모든 문자열 요소에 적용됩니다.

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>카탈로그 필드</b> </th> 
   <th class="entry"> <b>필드의 문자열 요소</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::ImageSet </span> </p> </td> 
   <td> <p>번역 가능한 문자열(',' ';' ':' 및/또는 필드의 시작/끝 조합으로 구분 기호로 구분된 모든 하위 요소). </p> <p> 현지화 가능 필드의 시작 부분에 있는 <span class="codeph"> 0xrggbb </span> 색상 값은 로컬라이제이션에서 제외되고 수정 없이 전달됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 카탈로그::맵 </span> </p> </td> 
   <td> <p>coords= 및 <span class="codeph"> shape= </span> <span class="codeph"> </span> 속성의 값을 제외한 모든 단일 또는 이중 인용 속성 값 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 카탈로그::대상 </span> </p> </td> 
   <td> <p>모든 <span class="codeph"> 대상의 값입니다.*.label </span> 및 <span class="codeph"> target.*.userdata </span> 속성. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 카탈로그::UserData </span> </p> </td> 
   <td> <p>모든 속성의 값입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 문자열 구문 {#section-d12320edf300409f8e17565b143acafc}

이미지 카탈로그의 현지화 활성화 *`string`* 요소는 각각 현지화 토큰이 앞에 있는 하나 이상의 현지화된 문자열로 구성됩니다.

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 문자열 <span class="varname"> 요소 </span></span> </p> </td> 
  <td class="stentry"> <p>[ <span class="varname"> defaultString </span>]*{ <span class="varname"> localizationToken </span> 지역화된 <span class="varname"> 문자열 </span>} </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 로컬라이제이션 <span class="varname"> 토큰 </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc= <span class="varname"> locStr </span> ^ </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> locId <span class="varname"> </span></span> </p> </td> 
  <td class="stentry"> <p>이 현지화 토큰 <span class="varname"> 다음에 </span> 지역화된 문자열에 대한 내부 <span class="varname"> 로케일 ID </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 현지화된 <span class="varname"> 문자열 </span></span> </p> </td> 
  <td class="stentry"> <p>현지화된 문자열. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> defaultString </span></span> </p> </td> 
  <td class="stentry"> <p>알 수 없는 로케일에 사용할 문자열입니다. </p> </td> 
 </tr> 
</table>

*`locId`* 는 ASCII여야 하며 &#39;^&#39;를 포함할 수 없습니다.

&#39;^&#39;는 HTTP 인코딩이 있거나 없는 하위 문자열의 어느 위치에서나 발생할 수 있습니다. 서버는 전체 *`localizationToken`* `^loc=locId^` 패턴과 일치하는 하위 문자열을 분리합니다.

*`stringElements`* 최소 하나 이상을 포함하지 않는 *`localizationToken`* 경우 현지화가 고려되지 않습니다.

## 번역 맵 {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` 서버가 클라이언트로 돌아갈 규칙을 *`localizedStrings`* 결정합니다. 입력 목록(로 지정된 값과 일치) *`locales`* 으로 구성되며, `locale=`*`locId`*&#x200B;각각 하나 이상의 내부 로케일 ID()가 없습니다. 예:

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

빈 *`locId`* 값은 가능한 경우 이 값이 반환되어야 *`defaultString`* 함을 나타냅니다.

자세한 내용은 의 설명을 `attribute::LocaleStrMap` 참조하십시오.

## 번역 프로세스 {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

위의 번역 맵과 요청의 예제가 `/is/image/myCat/myItem?req=&locale=nl`주어지면 서버는 먼저 로케일 맵에서 &quot; `nl`&quot;를 찾습니다. 일치하는 항목은 각 항목에 대해 `nl,N` 표시된 항목을 *`stringElement`*&#x200B;반환해야 함을 *`localizedString`* `^loc=N^` 나타냅니다. 이 값이 에 *`localizationToken`* 없으면 *`stringElement`*&#x200B;빈 값이 반환됩니다.

에 `catalog::UserData` 대해 다음을 `myCat/myItem` 포함한다고 가정해 보겠습니다(명확성을 위해 삽입된 줄 바꿈).

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

서버는 예제 요청에 대한 응답으로 다음을 반환합니다.

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## 알 수 없는 로케일 {#section-26dfeefbd60345de94bbfeaaf7741223}

위의 예에서 `attribute::LocaleStrMap` 빈 *`locale`* 값이 있는 항목이 있습니다. 서버는 이 항목을 사용하여 번역 맵에 명시적으로 지정되지 않은 모든 `locale=` 값을 처리합니다.

예제 번역 맵은 이러한 경우 사용 가능한 경우 반환되도록 *`defaultString`* 지정합니다. 따라서 이 번역 맵이 요청에 적용된 경우 다음 내용이 반환됩니다 `/is/image/myCat/myItem?req=&locale=ja`.

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## 예제 {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**언어 제품군**

여러 *`locId`* 값이 번역 맵의 각 값과 연결될 *`locale`* 수 있습니다. 이를 통해 대부분의 컨텐츠를 공통 기본 로케일(예: 국제 영어)을 사용하여 처리할 *`stringElements`* 때 선택할 수 있도록 국가별 또는 지역별 변형(예: 미국 영어 및 영국 영어)을 지원합니다.

예를 들어 미국 특정 영어( ` *`locId`* EUS`) 및 영국 전용 영어( ` *`locId)에 대한 지원을 추가하여`* EUK`경우에 따라 대체 철자를 지원하려고 합니다. 만약 EUK나 EUS가 존재하지 않는다면, 우리는 E로 돌아갈 것입니다.마찬가지로, 대부분의 시간 동안 오스트리아 특정 독일어 변형( `DAT`) *`localizedStrings`* 을 반환하면서 필요한 경우 사용할 수 `D`있습니다.

`attribute::LocaleStrMap` 다음과 같이 표시됩니다.

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

다음 표에서는 일부 대표 *`stringElement`* 및 *`locale`* 조합의 출력에 대해 설명합니다.

<table id="table_A6B67587C5F44B5E9CD0E7ED29A81198"> 
 <thead> 
  <tr> 
   <th class="entry"> <i>stringElement</i> </th> 
   <th class="entry"> <i>로케일</i> </th> 
   <th class="entry"> <p>출력 문자열 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^Loc=E^English^loc=D^German </span> </p> </td> 
   <td> <p> en,en_us, en_uk </p> <p> de, de_at, de_de </p> <p>기타 </p> </td> 
   <td> <p>영어 </p> <p>독일어 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^Loc=E^English^loc=KE^UK-English^loc=D^German^loc=DAT^Austrian </span> </p> </td> 
   <td> <p> en, en_us </p> <p> en_uk </p> <p> de, de_de </p> <p>de_at </p> <p>기타 </p> </td> 
   <td> <p>영어 </p> <p>영국-영어 </p> <p>독일어 </p> <p>오스트리아 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^Loc=en^English^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch </span> </p> <p> 이 예에서는 locId DDE <span class="varname"> 가 </span> attribute::LocaleStrMap에 없으므로 이 locId와 연결된 <span class="codeph"> 하위 </span>문자열이 반환되지 <span class="varname"> </span> 않습니다. </p> </td> 
   <td> <p> en, en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>기타 </p> </td> 
   <td> <p>영어 </p> <p>미국-영어 </p> <p>독일어 </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>

