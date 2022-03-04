---
description: 소스 개체 지정자입니다. 이미지, SVG 및 ICC 프로파일 객체는 이미지 카탈로그 항목 또는 상대 파일 경로로 지정할 수 있습니다
solution: Experience Manager
title: 개체
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 64846f8f-ebc6-446c-8277-04c45111dc24
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 1%

---

# 개체{#object}

소스 개체 지정자입니다. 이미지, SVG 및 ICC 프로파일 객체는 이미지 카탈로그 항목 또는 상대 파일 경로로 지정할 수 있습니다

`*`개체`*[/]{[ *`rootId`*/] *`objId`*}| *`경로`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId </span> </span> </p> </td> 
  <td class="stentry"> <p>이미지 카탈로그의 이름( <span class="codeph"> attribute::RootId </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objectId </span> </span> </p> </td> 
  <td class="stentry"> <p>지정한 기본 또는 기본 이미지 카탈로그의 이미지, SVG, 템플릿 또는 ICC 프로필 레코드의 id </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 경로 </span> </span> </p> </td> 
  <td class="stentry"> <p>상대 이미지, 마스크 또는 ICC 프로필 파일 경로 및 이름 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 개체 </span> </span> </p> </td> 
  <td class="stentry"> <p>은 기본 URL 경로나 <span class="codeph"> src= </span>, <span class="codeph"> 마스크= </span>, 또는 <span class="codeph"> icc= </span> 명령 </p> </td> 
 </tr> 
</table>

*`rootId`* 이미지 카탈로그를 식별합니다. (자세한 내용은 [이미지 카탈로그](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) 참조하십시오.) If *`rootId`* 은 URL 경로에 지정되며 해당 카탈로그는 *기본 카탈로그* 참조하십시오. 그렇지 않으면 기본 카탈로그가 기본 카탈로그로 사용됩니다. 동일한 요청에서 여러 개의 다른 이미지 카탈로그를 사용할 수 있습니다.

서버는 처음에 *`rootId`* 는 다음에서 생략됩니다. `src=`, `mask=`, 및 `icc=` 명령 및 은 기본 카탈로그에서 카탈로그 항목을 찾습니다. 서버에서 전체 *`object`* 문자열 *`objId.`*

카탈로그 항목이 있으면 사용됩니다. 그렇지 않으면 서버는 다음에 와 일치하려고 시도합니다 *`rootId`* 이미지 카탈로그 카탈로그가 식별되면 *`objId`*. 및 항목이 있으면 이 항목이 사용됩니다.

그렇지 않으면, *`object`* 는 명시적 파일 경로로 간주됩니다. 이 경우 `attribute::FullMatch` 기본 카탈로그에서 설정된 경우, 이 객체에 대해 카탈로그가 무시되고 대신 사용되는 기본 카탈로그가 무시됩니다. If `attribute::FullMatch` 가 설정되지 않은 경우 기본 카탈로그가 추가 처리에 사용됩니다.

둘 다 *`rootId`* 및 *`objId`* 는 대/소문자를 구분합니다. *`path`* 는 UNIX에서만 대/소문자를 구분합니다.

선행 `/` 을 지정하면 기본 카탈로그 대신 기본 카탈로그를 검색합니다. 이 기능은 주로 명시적 경로에 가 필요한 경우 유용합니다 `default::RootPath` 주요 카탈로그보다 `attribute::RootPath`를 사용할 수도 있지만 기본 카탈로그의 항목에 대한 액세스 권한을 얻을 수도 있습니다. 이 경우 기본 카탈로그의 항목에 의해 무시됩니다.

을(를) 참조하십시오. *콘텐츠 관리* 에서 *서버 구성 안내서* 자세한 내용은 *`path`* 물리적 파일 경로로 변환됩니다.

>[!NOTE]
>
>쉼표 &#39;,&#39; 문자는 사용할 수 없습니다. *`object.`*

## 지원되는 이미지 파일 형식 {#section-12c85aead78e4f759856ca9ff10637d7}

지원되는 파일 형식의 전체 목록은 IC(Image Converter) 유틸리티의 설명을 참조하십시오.

여러 해상도의 이미지 데이터가 필요한 응용 프로그램은 Dynamic Media 피라미드 TIFF(PTIF) 다중 해상도 형식을 사용할 때 가장 잘 수행됩니다. IC 유틸리티는 지원되는 이미지 포맷에서 PTIF 이미지를 생성하는 데 사용됩니다.

## 예제 {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**두 개의 서로 다른 이미지 카탈로그에서 이미지 및 ICC 프로파일 액세스**

&#39; 이미지를 검색합니다. [!DNL myImage]&#39;(으)로 식별된 이미지 카탈로그의 [!DNL myCatalog]&#39; 및 &#39; ICC 프로필 연결 [!DNL sRGB]이름이 &#39; 인 이미지 카탈로그에 있습니다. [!DNL myProfiles]&#39;:

` http:// *`서버`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

레이어링에 단일 이미지 카탈로그 사용

**&#39;에서 검색한 세 개의 레이어로 구성된 간단한 복합 이미지 작성 [!DNL myCatalog]&#39;:**

` http:// *`서버`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**카탈로그를 사용하여 속성을 제공하는 동안 이미지 파일에 직접 액세스**

액세스 [!DNL my/image/path/myImage.tif]에 구성된 기본 jpg 속성 사용 `myImageCatalog`:

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## 참조 {#section-b6eccefad63f441d922699c4aba58fc9}

[IC 유틸리티](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [마스크=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [attribute::FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
