---
description: 텍스트 문자열 현지화를 사용하면 이미지 카탈로그에 동일한 문자열 값에 대한 여러 로케일 특정 표현이 포함될 수 있습니다.
solution: Experience Manager
title: 텍스트 문자열 현지화
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: f105c7f2-b544-4c08-bb91-4916e485572d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 3%

---

# 텍스트 문자열 현지화{#text-string-localization}

텍스트 문자열 현지화를 사용하면 이미지 카탈로그에 동일한 문자열 값에 대한 여러 로케일 특정 표현이 포함될 수 있습니다.

서버는 `locale=`에 지정된 로케일과 일치하는 표현을 클라이언트에 반환하여 클라이언트측 현지화를 방지하고, IS 텍스트 요청으로 적절한 `locale=` 값을 보내기만 하면 응용 프로그램이 로케일을 전환할 수 있습니다.

## 범위 {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

텍스트 문자열 현지화는 다음 카탈로그 필드에 지역화 토큰 ` ^loc= *`locId`*^`을 포함하는 모든 문자열 요소에 적용됩니다.

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>카탈로그 필드</b> </th> 
   <th class="entry"> <b>필드의 문자열 요소</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 카탈로그::ImageSet  </span> </p> </td> 
   <td> <p>번역 가능한 문자열(',' ';' ':' 및/또는 필드의 시작/끝의 조합으로 구분)이 포함된 모든 하위 요소. </p> <p> 지역화 가능한 필드의 시작 부분에 있는 <span class="codeph"> 0xrggbb </span> 색상 값이 지역화에서 제외되고 수정 없이 전달됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 카탈로그::맵  </span> </p> </td> 
   <td> <p><span class="codeph"> coords= </span> 및 <span class="codeph"> shape= </span> 속성 값을 제외한 모든 단일 또는 이중 따옴표 속성 값 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 카탈로그::Target  </span> </p> </td> 
   <td> <p><span class="codeph"> 대상의 값입니다.*.label </span> 및 <span class="codeph"> target.*.userdata </span> 속성을 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 카탈로그::UserData  </span> </p> </td> 
   <td> <p>모든 속성의 값입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 문자열 구문 {#section-d12320edf300409f8e17565b143acafc}

이미지 카탈로그의 로컬라이제이션이 활성화된 *`string`* 요소는 각각 현지화 토큰 앞에 있는 하나 이상의 현지화된 문자열로 구성됩니다.

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> stringElement  </span> </span> </p> </td> 
  <td class="stentry"> <p>[ <span class="varname"> defaultString </span>]*{ <span class="varname"> localizationToken </span> <span class="varname"> localizedString </span>} </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizationToken  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc=  <span class="varname"> locStr  </span> ^  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId  </span> </span> </p> </td> 
  <td class="stentry"> <p>이 <span class="varname"> localizationToken </span> 다음에 나오는 <span class="varname"> localizedString </span>에 대한 내부 로케일 ID입니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizedString  </span> </span> </p> </td> 
  <td class="stentry"> <p>현지화된 문자열입니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> defaultString  </span> </span> </p> </td> 
  <td class="stentry"> <p>알 수 없는 로케일에 사용할 문자열입니다. </p> </td> 
 </tr> 
</table>

*`locId`* ASCII여야 하며 &#39;^&#39;를 포함할 수 없습니다.

&#39;^&#39;는 HTTP 인코딩이 있거나 없는 하위 문자열의 모든 위치에서 발생할 수 있습니다. 서버는 전체 *`localizationToken`* `^loc=locId^` 패턴과 일치하여 별도의 하위 문자열을 만듭니다.

*`stringElements`* 적어도 하나 이상의 지역화 *`localizationToken`* 에 포함되지 않은 항목은 지역화용으로 간주되지 않습니다.

## 번역 맵 {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` 는 서버가 클라이언트로 반환할 규칙 *`localizedStrings`* 을 결정합니다. 입력 *`locales`* 목록(`locale=`로 지정된 값과 일치)으로 구성되며, 각각 하나 이상의 내부 로케일 ID( *`locId`*)가 없습니다. 예:

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

빈 *`locId`* 값은 *`defaultString`* 가 반환되어야 하는 경우(가능한 경우) 나타냅니다.

자세한 내용은 `attribute::LocaleStrMap` 설명을 참조하십시오.

## 번역 프로세스 {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

위의 번역 맵 예와 요청 `/is/image/myCat/myItem?req=&locale=nl`이 주어지면 서버는 먼저 로케일 맵에서 &quot; `nl`&quot;를 찾습니다. 일치하는 항목 `nl,N`은 각 *`stringElement`*&#x200B;에 대해 `^loc=N^`로 표시된 *`localizedString`*&#x200B;가 반환됨을 나타냅니다. 이 *`localizationToken`*&#x200B;이 *`stringElement`*&#x200B;에 없으면 빈 값이 반환됩니다.

`myCat/myItem`에 대해 `catalog::UserData`에 다음(명확성을 위해 삽입된 줄 바꿈)이 포함되어 있다고 가정해 보겠습니다.

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

서버는 예제 요청에 응답하여 다음을 반환합니다.

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## 알 수 없는 로케일 {#section-26dfeefbd60345de94bbfeaaf7741223}

위의 예에서 `attribute::LocaleStrMap`에는 빈 *`locale`* 값이 있는 항목이 있습니다. 서버는 이 항목을 사용하여 번역 맵에 명시적으로 지정되지 않은 모든 `locale=` 값을 처리합니다.

번역 맵 예는 이 경우 *`defaultString`*&#x200B;이(가) 가능한 경우 반환되도록 지정합니다. 따라서 이 번역 맵이 요청 `/is/image/myCat/myItem?req=&locale=ja`에 적용된 경우 다음과 같이 반환됩니다.

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## 예제 {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**언어 가족**

여러 *`locId`* 값은 번역 맵의 각 *`locale`*&#x200B;과 연결될 수 있습니다. 이렇게 하면 공통 기본 로케일(예: 국제 영어)로 대부분의 컨텐츠를 처리하는 동안 국가별 또는 지역별 변형(예: 미국 영어 및 영국 영어)을 선택 *`stringElements`*&#x200B;에 지원할 수 있습니다.

이 예에서는 미국별 영어( `*`locId`* EUS`)와 영국별 영어( `*`locId`* EUK`)에 대한 지원을 추가하여 경우에 따라 대체 철자를 지원하려고 합니다. EUK 또는 EUS가 없는 경우 E로 폴백합니다. 마찬가지로, 대부분의 경우 일반 독일어 *`localizedStrings`*(`D`로 표시됨)를 반환하는 동안 필요한 경우 오스트리아별 독일어 변형( `DAT`)을 사용할 수 있습니다.

`attribute::LocaleStrMap` 다음과 같습니다.

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

다음 표에서는 일부 대표자 *`stringElement`* 및 *`locale`* 조합의 출력에 대해 설명합니다.

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
   <td> <p> <span class="codeph"> ^loc=E^English^loc=D^독일어  </span> </p> </td> 
   <td> <p> en,en_us, en_uk </p> <p> de, de_at, de_de </p> <p>기타 </p> </td> 
   <td> <p>영어 </p> <p>독일어 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=UKE^UK-English^loc=D^German^loc=DAT^오스트리아  </span> </p> </td> 
   <td> <p> en, en_us </p> <p> en_uk </p> <p> de, de_de </p> <p>de_at </p> <p>기타 </p> </td> 
   <td> <p>영어 </p> <p>영국-영어 </p> <p>독일어 </p> <p>오스트리아 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=en^English^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch  </span> </p> <p> 이 예제에서 <span class="varname"> locId </span> DDE가 <span class="codeph"> 속성::LocaleStrMap </span>에 없으므로 이 <span class="varname"> locId </span>와 연결된 하위 문자열은 반환되지 않습니다. </p> </td> 
   <td> <p> en, en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>기타 </p> </td> 
   <td> <p>영어 </p> <p>미국-영어 </p> <p>독일어 </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>
