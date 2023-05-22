---
description: 텍스트 문자열 로컬라이제이션을 사용하면 이미지 카탈로그에 동일한 문자열 값에 대한 여러 로케일별 표현을 포함할 수 있습니다.
solution: Experience Manager
title: 텍스트 문자열 로컬라이제이션
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f105c7f2-b544-4c08-bb91-4916e485572d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '666'
ht-degree: 3%

---

# 텍스트 문자열 로컬라이제이션{#text-string-localization}

텍스트 문자열 로컬라이제이션을 사용하면 이미지 카탈로그에 동일한 문자열 값에 대한 여러 로케일별 표현을 포함할 수 있습니다.

서버는 지정된 로케일과 일치하는 표현을 클라이언트로 반환합니다 `locale=`를 사용하면 클라이언트측 현지화를 방지하고 적절한 를 보냄으로써 애플리케이션에서 로케일을 전환할 수 있습니다 `locale=` IS 텍스트 요청이 포함된 값.

## 범위 {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

텍스트 문자열 지역화는 지역화 토큰을 포함하는 모든 문자열 요소에 적용됩니다 ` ^loc= *`locId`*^` 다음 카탈로그 필드:

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
   <td> <p>변환 가능한 문자열을 포함하는 모든 하위 요소(',' ';' ':' 및/또는 필드의 시작/끝 구분 기호의 조합으로 구분). </p> <p> A <span class="codeph"> 0xrrggbb </span> 현지화 가능 필드의 시작 부분에 있는 색상 값은 현지화에서 제외되며 수정 없이 전달됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Map </span> </p> </td> 
   <td> <p>의 값을 제외한 모든 작은따옴표 또는 큰따옴표 속성 값 <span class="codeph"> 코드= </span> 및 <span class="codeph"> shape= </span> 속성. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Target </span> </p> </td> 
   <td> <p>임의 값 <span class="codeph"> 타겟.*.label </span> 및 <span class="codeph"> 타겟.*.userdata </span> 속성. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::UserData </span> </p> </td> 
   <td> <p>모든 속성의 값입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 문자열 구문 {#section-d12320edf300409f8e17565b143acafc}

현지화 사용 *`string`* 이미지 카탈로그의 요소는 하나 이상의 현지화된 문자열로 구성되며, 각 문자열에는 현지화 토큰이 앞에 옵니다.

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> stringElement </span> </span> </p> </td> 
  <td class="stentry"> <p>[ <span class="varname"> defaultString </span>]*{ <span class="varname"> localizationToken </span> <span class="varname"> localizedString </span>} </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizationToken </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc= <span class="varname"> locStr </span> ^ </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId </span> </span> </p> </td> 
  <td class="stentry"> <p>에 대한 내부 로케일 ID <span class="varname"> localizedString </span> 팔로우하는 중 <span class="varname"> localizationToken </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizedString </span> </span> </p> </td> 
  <td class="stentry"> <p>지역화된 문자열입니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> defaultString </span> </span> </p> </td> 
  <td class="stentry"> <p>알 수 없는 로케일에 사용할 문자열입니다. </p> </td> 
 </tr> 
</table>

*`locId`* 은(는) ASCII여야 하며 &#39;^&#39;을(를) 포함할 수 없습니다.

&#39;^&#39;은(는) HTTP 인코딩이 있거나 없는 하위 문자열의 모든 위치에서 발생할 수 있습니다. 서버가 전체 서버와 일치함 *`localizationToken`* `^loc=locId^` 패턴을 사용하여 하위 문자열을 구분하십시오.

*`stringElements`* 적어도 1개는 포함하지 아니한다 *`localizationToken`* 현지화 대상으로 간주되지 않습니다.

## 번역 맵 {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` 서버에서 사용하는 규칙을 정의하여 *`localizedStrings`* 클라이언트로 돌아갑니다. 입력 목록으로 구성됩니다 *`locales`* (지정된 값과 일치) `locale=`)에 포함된 각 내부 로케일 id가 없습니다( *`locId`*). 예:

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

비어 있음 *`locId`* 값은 이 *`defaultString`* 가능한 경우 반환됩니다.

다음에 대한 설명을 참조하십시오. `attribute::LocaleStrMap` 을 참조하십시오.

## 번역 프로세스 {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

위의 예제 번역 맵 및 요청에 따라 `/is/image/myCat/myItem?req=&locale=nl`, 서버는 먼저 &quot; `nl`로케일 맵에서 &quot;&quot;입니다. 일치하는 항목 `nl,N` 각각에 대해 를 나타냅니다. *`stringElement`*, *`localizedString`* 다음으로 표시 `^loc=N^` 반환해야 합니다. 다음과 같은 경우 *`localizationToken`* 이(가)에 없습니다. *`stringElement`*&#x200B;를 입력하면 빈 값이 반환됩니다.

예: `catalog::UserData` 대상 `myCat/myItem` 에는 다음 항목이 포함되어 있습니다(명확하게 하기 위해 줄 바꿈을 삽입함).

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

서버는 예제 요청에 대한 응답으로 다음을 반환합니다.

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## 알 수 없는 로케일 {#section-26dfeefbd60345de94bbfeaaf7741223}

위의 예에서, `attribute::LocaleStrMap` 이(가) 비어 있는 항목이 있습니다. *`locale`* 값. 서버는 이 항목을 사용하여 모든 항목을 처리합니다 `locale=` 번역 맵에서 명시적으로 지정되지 않은 값.

예제 번역 맵은 이러한 경우 *`defaultString`* 가능한 경우 반환됩니다. 따라서 이 번역 맵이 요청에 적용되면 다음이 반환됩니다 `/is/image/myCat/myItem?req=&locale=ja`:

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## 예제 {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**언어 계열**

복수 *`locId`* 값은 다음과 연관될 수 있습니다. *`locale`* 번역 맵에서. 이를 통해 선택한 국가별 또는 지역별 변형(예: 미국 영어 대 영국 영어)을 지원할 수 있습니다 *`stringElements`* 일반적인 기본 로케일로 대부분의 콘텐츠를 처리하는 동안(예: 국제 영어).

이 예제에서는 미국별 영어( )에 대한 지원을 추가하려고 합니다 `*`locId`* EUS`) 및 UK 전용 영어( `*`locId`* EUK`)을 클릭하여 대체 철자를 가끔씩 사용할 수 있습니다. 만약 EUK나 EUS가 존재하지 않는다면, 우리는 E로 후퇴할 것이다. 이와 유사하게, 오스트리아에 특유한 독일어 변형들( `DAT`)은 일반적인 독일어를 반환할 때 필요한 경우 사용할 수 있습니다 *`localizedStrings`* (다음으로 표시됨) `D`) 대부분의 경우.

`attribute::LocaleStrMap` 은 다음과 같이 표시됩니다.

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

다음 표에서는 몇 가지 예에 대한 출력을 설명합니다. *`stringElement`* 및 *`locale`* 조합:

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
   <td> <p> <span class="codeph"> ^loc=E^English^loc=D^German </span> </p> </td> 
   <td> <p> en,en_us, en_uk </p> <p> de, de_at, de_de </p> <p>다른 모든 항목 </p> </td> 
   <td> <p>영어 </p> <p>독일어 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=UKE^UK-English^loc=D^German^loc=DAT^Austrian </span> </p> </td> 
   <td> <p> en, en_us </p> <p> en_uk </p> <p> de, de_de </p> <p>de_at </p> <p>다른 모든 항목 </p> </td> 
   <td> <p>영어 </p> <p>UK-영어 </p> <p>독일어 </p> <p>오스트리아어 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=en^English^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch </span> </p> <p> 이 예제의 경우 <span class="varname"> locId </span> DDE가에 존재하지 않음 <span class="codeph"> attribute::LocaleStrMap </span>, 따라서 이와 연결된 하위 문자열 <span class="varname"> locId </span> 은(는) 반환되지 않습니다. </p> </td> 
   <td> <p> en, en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>다른 모든 항목 </p> </td> 
   <td> <p>영어 </p> <p>미국-영어 </p> <p>독일어 </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>
