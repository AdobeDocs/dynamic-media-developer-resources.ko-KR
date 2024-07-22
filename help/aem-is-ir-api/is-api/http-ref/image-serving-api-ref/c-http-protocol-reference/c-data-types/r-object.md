---
description: Source 개체 지정자입니다. 이미지, SVG 및 ICC 프로파일 객체는 이미지 카탈로그 항목 또는 상대 파일 경로로 지정할 수 있습니다
solution: Experience Manager
title: 개체
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 64846f8f-ebc6-446c-8277-04c45111dc24
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 1%

---

# 개체{#object}

Source 개체 지정자입니다. 이미지, SVG 및 ICC 프로파일 객체는 이미지 카탈로그 항목 또는 상대 파일 경로로 지정할 수 있습니다

`*`개체`*[/]{[ *`rootId`*/] *`objId`*}| *`경로`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId </span> </span> </p> </td> 
  <td class="stentry"> <p>이미지 카탈로그 이름( <span class="codeph"> 특성::RootId </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objtId </span> </span> </p> </td> 
  <td class="stentry"> <p>지정된, 기본 또는 기본 이미지 카탈로그에 있는 이미지, SVG, 템플릿 또는 ICC 프로필 레코드의 ID </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 경로 </span> </span> </p> </td> 
  <td class="stentry"> <p>상대 이미지, 마스크 또는 ICC 프로파일 파일 경로 및 이름 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 개체 </span> </span> </p> </td> 
  <td class="stentry"> <p>기본 URL 경로 또는 <span class="codeph"> src= </span>, <span class="codeph"> mask= </span> 또는 <span class="codeph"> icc= </span> 명령에서 발생할 수 있습니다. </p> </td> 
 </tr> 
</table>

*`rootId`*&#x200B;이(가) 이미지 카탈로그를 식별합니다. 자세한 내용은 [이미지 카탈로그](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)를 참조하세요. URL 경로에 *`rootId`*&#x200B;이(가) 지정되어 있으면 해당 카탈로그가 이 요청의 *기본 카탈로그*&#x200B;가 됩니다. 그렇지 않으면 기본 카탈로그가 기본 카탈로그로 사용됩니다. 동일한 요청에서 여러 개의 다른 이미지 카탈로그를 사용할 수 있습니다.

서버는 처음에 `src=`, `mask=` 및 `icc=` 명령에서 *`rootId`*&#x200B;이(가) 생략되었다고 가정하고 기본 카탈로그에서 카탈로그 항목을 찾으려고 시도합니다. 사실상, 서버는 전체 *`object`* 문자열을 *`objId.`*(으)로 사용하려고 합니다.

카탈로그 항목이 발견되면 이 항목이 사용됩니다. 그렇지 않으면 서버는 다음에 이미지 카탈로그의 *`rootId`*&#x200B;과(와) 일치하려고 시도합니다. 카탈로그가 식별되면 *`objId`*&#x200B;을(를) 검색합니다. 및 항목이 발견되면 사용됩니다.

그렇지 않으면 *`object`*&#x200B;이(가) 명시적 파일 경로로 간주됩니다. 이 경우 `attribute::FullMatch`이(가) 기본 카탈로그에 설정되어 있으면 이 개체에 대한 카탈로그가 무시되고 대신 기본 카탈로그가 사용됩니다. `attribute::FullMatch`이(가) 설정되지 않은 경우 추가 처리에 기본 카탈로그를 사용합니다.

*`rootId`*&#x200B;과(와) *`objId`*&#x200B;은(는) 모두 대/소문자를 구분합니다. *`path`*&#x200B;은(는) UNIX에서만 대/소문자를 구분합니다.

선행 `/`이(가) 지정된 경우 주 카탈로그 대신 기본 카탈로그가 검색됩니다. 이 기능은 주로 명시적 경로에 기본 카탈로그의 `attribute::RootPath`이(가) 아닌 `default::RootPath`이(가) 필요한 경우에 유용하지만, 기본 카탈로그의 항목에 의해 재정의되는 기본 카탈로그의 항목에 대한 액세스 권한을 얻는 데 사용할 수도 있습니다.

*`path`*&#x200B;을(를) 실제 파일 경로로 변환하는 방법에 대한 자세한 내용은 *서버 구성 가이드*&#x200B;의 *콘텐츠 관리*&#x200B;를 참조하십시오.

>[!NOTE]
>
>*`object.`*&#x200B;에는 쉼표 &#39;,&#39; 문자를 사용할 수 없습니다.

## 지원되는 이미지 파일 형식 {#section-12c85aead78e4f759856ca9ff10637d7}

지원되는 파일 형식의 전체 목록은 IC(이미지 변환기) 유틸리티의 설명을 참조하십시오.

여러 해상도의 이미지 데이터가 필요한 응용 프로그램은 Dynamic Media 피라미드 TIFF(PTIF) 다중 해상도 형식을 사용할 때 가장 잘 수행됩니다. IC 유틸리티는 지원되는 모든 이미지 형식에서 PTIF 이미지를 만드는 데 사용됩니다.

## 예제 {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**두 개의 다른 이미지 카탈로그에서 이미지 및 ICC 프로필에 액세스**

&#39; [!DNL myCatalog]&#39;(으)로 식별된 이미지 카탈로그에서 &#39; [!DNL myImage]&#39; 이미지를 검색하고 이름이 &#39; [!DNL myProfiles]&#39;인 이미지 카탈로그에 있는 ICC 프로필 &#39; [!DNL sRGB]&#39;을(를) 연결합니다.

` http:// *`서버`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

계층화로 단일 이미지 카탈로그 사용

**세 개의 레이어로 구성된 간단한 합성 이미지를 만듭니다. 모두 &#39;[!DNL myCatalog]&#39;에서 검색됩니다.**

` http:// *`서버`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**특성을 제공하기 위해 카탈로그를 계속 사용하는 동안 이미지 파일에 직접 액세스**

`myImageCatalog`에 구성된 기본 jpg 특성을 사용하여 [!DNL my/image/path/myImage.tif]에 액세스:

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## 참조 {#section-b6eccefad63f441d922699c4aba58fc9}

[IC 유틸리티](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [마스크=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [특성::FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
