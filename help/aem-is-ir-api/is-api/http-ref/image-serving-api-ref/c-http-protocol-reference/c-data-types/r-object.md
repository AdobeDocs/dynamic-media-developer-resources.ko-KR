---
description: 소스 개체 지정자. 이미지, SVG 및 ICC 프로필 개체는 이미지 카탈로그 항목 또는 상대 파일 경로로 지정할 수 있습니다.
seo-description: 소스 개체 지정자. 이미지, SVG 및 ICC 프로필 개체는 이미지 카탈로그 항목 또는 상대 파일 경로로 지정할 수 있습니다.
seo-title: 개체
solution: Experience Manager
title: 개체
topic: Scene7 Image Serving - Image Rendering API
uuid: 8d25b47d-0f23-4d9a-a7e6-6e865ae4114e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 개체{#object}

소스 개체 지정자. 이미지, SVG 및 ICC 프로필 개체는 이미지 카탈로그 항목 또는 상대 파일 경로로 지정할 수 있습니다.

` *``*[/]{[ *``*/] *``*}| *`objectrootIdobjIdpath`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 루트 ID </span></span> </p> </td> 
  <td class="stentry"> <p>이미지 카탈로그의 이름( <span class="codeph"> 속성::RootId </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 개체 ID </span></span> </p> </td> 
  <td class="stentry"> <p>지정된, 기본 또는 기본 이미지 카탈로그의 이미지, SVG, 템플릿 또는 ICC 프로필 레코드 ID </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 경로 </span></span> </p> </td> 
  <td class="stentry"> <p>상대 이미지, 마스크 또는 ICC 프로필 파일 경로 및 이름 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 개체 </span></span> </p> </td> 
  <td class="stentry"> <p>기본 URL 경로나 <span class="codeph"> src= </span>, <span class="codeph"> mask= </span>또는 <span class="codeph"> icc= </span> 명령에서 발생할 수 있습니다. </p> </td> 
 </tr> 
</table>

*`rootId`* 이미지 카탈로그를 식별합니다. (See [Image Catalog](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) for details.) URL 경로에 *`rootId`* 지정된 경우 해당 카탈로그는 이 요청에 대한 *기본 카탈로그가* 됩니다. 그렇지 않으면 기본 카탈로그가 기본 카탈로그로 사용됩니다. 동일한 요청에서 여러 개의 서로 다른 이미지 카탈로그를 사용할 수 있습니다.

서버는 처음에 *`rootId`* , `src=`및 `mask=``icc=` 명령에서 생략되었다고 가정하고 기본 카탈로그에서 카탈로그 항목을 찾으려고 시도합니다. 실제로 서버는 전체 *`object`* 문자열을 *`objId.`*

카탈로그 항목이 발견되면 사용됩니다.그렇지 않은 경우 서버는 다음에 이미지 카탈로그의 *`rootId`* 일치 여부를 시도합니다. 카탈로그가 식별되면, 카탈로그가 검색됩니다 *`objId`*. 및 항목이 있으면 사용됩니다.

그렇지 않으면 *`object`* 는 명시적 파일 경로로 간주됩니다. 이 경우 기본 카탈로그에 `attribute::FullMatch` 설정된 경우 이 개체에 대해 카탈로그가 무시되고 대신 기본 카탈로그가 사용됩니다. 이 `attribute::FullMatch` 설정되지 않은 경우 기본 카탈로그가 추가 처리에 사용됩니다.

대/ *`rootId`* 소문자를 *`objId`* 구분합니다. *`path`* 은 UNIX에서만 대/소문자를 구분합니다.

행간 &#39;/&#39;를 지정하면 기본 카탈로그 대신 기본 카탈로그를 검색합니다. 이 기능은 기본적으로 기본 카탈로그가 `default::RootPath` 아닌 명시적 경로가 필요한 `attribute::RootPath`경우 유용하지만 기본 카탈로그의 항목에 대한 액세스를 얻는 데 사용할 수도 있습니다. 기본 카탈로그의 항목에서는 무시될 수 있습니다.

실제 파일 *경로로* 변환하는 방법에 대한 *자세한* 내용은 서버 구성 안내서의 *`path`* 컨텐츠관리를 참조하십시오.

>[!NOTE]
>
>쉼표 &#39;,&#39; 문자는 *`object.`*

## 지원되는 이미지 파일 포맷 {#section-12c85aead78e4f759856ca9ff10637d7}

지원되는 파일 포맷의 전체 목록은 IC(Image Converter) 유틸리티의 설명을 참조하십시오.

여러 해상도의 이미지 데이터가 필요한 응용 프로그램은 Scene7 피라미드 TIFF(다중 해상도) 형식을 사용할 때 가장 잘 수행됩니다. IC 유틸리티는 지원되는 모든 이미지 형식에서 TIF 이미지를 만드는 데 사용됩니다.

## 예제 {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**두 개의 서로 다른 이미지 카탈로그에서 이미지 및 ICC 프로필 액세스**

이미지 카탈로그에서 &#39; [!DNL myImage]&#39; 이미지를 [!DNL myCatalog]검색하고 이름이 &#39; [!DNL sRGB][!DNL myProfiles]&#39;인 이미지 카탈로그에 있는 ICC 프로필 &#39;&#39;을(를) 첨부합니다.

` http:// *`서버`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

레이어링을 사용하여 단일 이미지 카탈로그 사용

**모두 &#39;[!DNL myCatalog]&#39;에서 검색된 세 개의 레이어로 구성된 간단한 합성 이미지를 만듭니다.**

` http:// *`서버`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**카탈로그를 사용하여 속성을 제공하는 동안 이미지 파일에 직접 액세스**

다음 위치에 구성된 기본 jpg 속성을 사용하여 [!DNL my/image/path/myImage.tif]액세스합니다. `myImageCatalog`

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## 참조 {#section-b6eccefad63f441d922699c4aba58fc9}

[IC 유틸리티](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [속성::FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
