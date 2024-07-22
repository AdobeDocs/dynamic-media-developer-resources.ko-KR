---
title: 텍스트 문자열 로컬라이제이션
description: 텍스트 문자열 지역화를 사용하면 이미지 카탈로그에 동일한 문자열 값에 대한 여러 로케일별 표현을 포함할 수 있습니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f105c7f2-b544-4c08-bb91-4916e485572d
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 1%

---

# 텍스트 문자열 로컬라이제이션{#text-string-localization}

텍스트 문자열 지역화를 사용하면 이미지 카탈로그에 동일한 문자열 값에 대한 여러 로케일별 표현을 포함할 수 있습니다.

서버가 `locale=`(으)로 지정된 로캘과 일치하는 표현을 클라이언트에 반환하여 클라이언트측 지역화를 방지하고 IS 텍스트 요청을 사용하여 적절한 `locale=` 값을 보냄으로써 응용 프로그램이 로캘을 전환할 수 있도록 합니다.

## 범위 {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

다음 카탈로그 필드에 지역화 토큰 ` ^loc= *`locId`*^`을(를) 포함하는 모든 문자열 요소에 텍스트 문자열 지역화가 적용됩니다.

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>카탈로그 필드</b> </th> 
   <th class="entry"> <b>필드의 문자열 요소</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 카탈로그::ImageSet </span> </p> </td> 
   <td> <p>변환 가능한 문자열을 포함하는 모든 하위 요소(',' ';' ':' 및/또는 필드의 시작/끝 구분 기호의 조합으로 구분). </p> <p> 지역화할 수 있는 필드의 시작 부분에 있는 <span class="codeph"> 0xrrggbb </span> 색 값이 지역화에서 제외되며 수정 없이 통과됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 카탈로그::맵 </span> </p> </td> 
   <td> <p><span class="codeph"> 코드= </span> 및 <span class="codeph"> 셰이프= </span> 특성의 값을 제외한 모든 작은따옴표 또는 큰따옴표 특성 값입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 카탈로그::대상 </span> </p> </td> 
   <td> <p><span class="codeph"> 대상의 값입니다.*.label </span> 및 <span class="codeph"> 대상.*.userdata </span> 속성입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 카탈로그::UserData </span> </p> </td> 
   <td> <p>모든 속성의 값입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 문자열 구문 {#section-d12320edf300409f8e17565b143acafc}

이미지 카탈로그의 로컬라이제이션 사용 *`string`* 요소는 하나 이상의 로컬라이제이션 문자열로 구성되며, 각 문자열에는 로컬라이제이션 토큰이 옵니다.

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> stringElement </span> </span> </p> </td> 
  <td class="stentry"> <p><span class="varname"> defaultString </span>]*{ <span class="varname"> localizationToken </span> <span class="varname"> localizedString </span> </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizationToken </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc= <span class="varname"> locStr </span> ^ </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId </span> </span> </p> </td> 
  <td class="stentry"> <p>이 <span class="varname"> localizationToken </span> 다음에 오는 <span class="varname"> localizedString </span>의 내부 로캘 ID입니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 지역화된 문자열 </span> </span> </p> </td> 
  <td class="stentry"> <p>지역화된 문자열입니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> defaultString </span> </span> </p> </td> 
  <td class="stentry"> <p>알 수 없는 로케일에 사용할 문자열입니다. </p> </td> 
 </tr> 
</table>

*`locId`*&#x200B;은(는) ASCII여야 하며 &#39;^&#39;을(를) 포함할 수 없습니다.

&#39;^&#39;은(는) HTTP 인코딩이 있거나 없는 하위 문자열의 모든 위치에서 발생할 수 있습니다. 서버가 전체 *`localizationToken`* `^loc=locId^` 패턴과 일치하여 별도의 하위 문자열을 찾습니다.

하나 이상의 *`localizationToken`*&#x200B;을(를) 포함하지 않는 *`stringElements`*&#x200B;은(는) 현지화 대상으로 간주되지 않습니다.

## 번역 맵 {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap`은(는) 클라이언트에 반환할 *`localizedStrings`*&#x200B;을(를) 결정하기 위해 서버에서 사용하는 규칙을 정의합니다. 이 ID는 각각 내부 로캘 ID( *`locId`*)가 없는 *`locales`* 입력(`locale=`(으)로 지정된 값과 일치)로 구성됩니다. 예:

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

빈 *`locId`* 값은 사용 가능한 경우 *`defaultString`*&#x200B;이(가) 반환되어야 함을 나타냅니다.

자세한 내용은 `attribute::LocaleStrMap`의 설명을 참조하세요.

## 번역 프로세스 {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

위의 예제 번역 맵과 `/is/image/myCat/myItem?req=&locale=nl` 요청이 주어지면 서버는 먼저 로케일 맵에서 &quot; `nl`&quot;을(를) 찾습니다. 일치하는 항목 `nl,N`은(는) 각 *`stringElement`*&#x200B;에 대해 `^loc=N^`(으)로 표시된 *`localizedString`*&#x200B;이(가) 반환되어야 함을 나타냅니다. 이 *`localizationToken`*&#x200B;이(가) *`stringElement`*&#x200B;에 없으면 빈 값이 반환됩니다.

`myCat/myItem`에 대한 `catalog::UserData`에 다음 내용이 포함되어 있다고 가정합니다(명확성을 위해 줄 바꿈을 삽입함).

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

서버는 예제 요청에 대한 응답으로 다음을 반환합니다.

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## 알 수 없는 로케일 {#section-26dfeefbd60345de94bbfeaaf7741223}

위의 예에서 `attribute::LocaleStrMap`에 빈 *`locale`* 값이 있는 항목이 있습니다. 서버는 이 항목을 사용하여 번역 맵에서 명시적으로 지정되지 않은 모든 `locale=` 값을 처리합니다.

예제 번역 맵은 이러한 경우 *`defaultString`*&#x200B;이(가) 반환되도록 지정합니다(사용 가능한 경우). 따라서 이 번역 맵이 요청 `/is/image/myCat/myItem?req=&locale=ja`에 적용되면 다음 항목이 반환됩니다.

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## 예제 {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**언어 계열**

여러 *`locId`* 값이 번역 맵의 각 *`locale`*&#x200B;과(와) 연결되어 있을 수 있습니다. 일반적인 기본 로케일(예: 국제 영어)로 대부분의 콘텐츠를 처리하면서 선택한 *`stringElements`*&#x200B;에 대해 국가별 또는 지역별 변형(예: 미국 영어 대 영국 영어)을 지원할 수 있기 때문입니다.

예를 들어 가끔씩 대체 철자를 지원하기 위해 미국별 영어(`*`locId`* EUS`)와 영국별 영어(`*`locId`* EUK`)에 대한 지원이 추가되었습니다. EUK 또는 EUS가 없는 경우 E로 대체됩니다. 마찬가지로 대부분의 경우 일반적인 독일어 *`localizedStrings`*(`D`(으)로 표시됨)을(를) 반환하는 동안 필요한 경우 오스트리아별 독일어 변형(`DAT`)을 사용할 수 있습니다.

`attribute::LocaleStrMap`은(는) 다음과 같이 표시됩니다.

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

다음 표에서는 일부 대표적인 *`stringElement`* 및 *`locale`* 조합의 출력을 설명합니다.

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
   <td> <p> en, en_us, en_uk </p> <p> de, de_at, de_de </p> <p>다른 모든 항목 </p> </td> 
   <td> <p>영어 </p> <p>독일어 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=UKE^UK-English^loc=D^German^loc=DAT^Austrian </span> </p> </td> 
   <td> <p> en, en_us </p> <p> en_uk </p> <p> de, de_de </p> <p>de_at </p> <p>다른 모든 항목 </p> </td> 
   <td> <p>영어 </p> <p>UK-영어 </p> <p>독일어 </p> <p>오스트리아어 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=en^English^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch </span> </p> <p> 이 예제의 경우 <span class="varname"> locId </span> DDE가 <span class="codeph"> 특성::LocaleStrMap </span>에 없으므로 이 <span class="varname"> locId </span>과(와) 연결된 하위 문자열이 반환되지 않습니다. </p> </td> 
   <td> <p> en, en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>다른 모든 항목 </p> </td> 
   <td> <p>영어 </p> <p>미국-영어 </p> <p>독일어 </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>
