---
description: 배경색을 봅니다. 합성 이미지(이미지 보기)의 배경색을 지정합니다.
solution: Experience Manager
title: bgc
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39ca0d63-55c6-40be-88b6-cf73828cc355
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 2%

---

# bgc{#bgc}

배경색을 봅니다. 합성 이미지(이미지 보기)의 배경색을 지정합니다.

`bgc= *`color`*`

<table id="simpletable_998CF426296945FEA48D19E33B71A17E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 색상</span></span> </p> </td> 
  <td class="stentry"> <p>회색, RGB 또는 CMYK 색상 값. </p></td> 
 </tr> 
</table>

보기 배경에 사용할 불투명 채우기 색상을 지정합니다. 합성 이미지에 투명 영역이 있거나 합성 이미지의 종횡비가 보기 사각형과 다른 경우에만 표시됩니다. 다음과 같은 경우 무시됨 `fmt=tif-alpha` 또는 `fmt=png-alpha`, 또는 `req=mask`.

>[!NOTE]
>
>&#39;s&#39; 색상 접미사는 다음에 의해 무시됩니다. `bgc=`. 색상 값 지정 `bgc=` 는 항상 해당 출력 색상 공간과 연결됩니다.

## 속성 {#section-b729b50b1ea7433b82ba34ecd61839cd}

속성 보기. 현재 레이어 설정에 관계없이 적용됩니다. 다음과 같은 경우 무시됨 `req=mask`, `fmt=tif-alpha`, `fmt=png-alpha`, `fmt=gif-alpha`, 또는 `fmt=swf-alpha`.

색상으로 지정된 모든 알파 값은 무시됩니다.

*`color`* 은 출력 색상 공간에 속한다고 가정합니다(에 지정된 대로). `icc=`) 및 의 픽셀 유형은 출력 이미지와 동일해야 합니다. 픽셀 유형이 일치하지 않으면, *`color`* 는 순진 변환을 사용하여 변환됩니다.

## 기본값 {#section-4e025cbd723547b5ab4450f7aad70da3}

`attribute::BkgColor`.

## 예 {#section-7bcdfbc0e1274e86a69d39186b090789}

썸네일 요청에 대한 명시적 배경색을 지정합니다.

`http://server/myRootId/myImageId?req=tmb&bgc=214,245,130`

## 참조 {#section-1e55f9f98f1847918a1725836a27cfaa}

[색상](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93), [attribute::BkgColor](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-bkgcolor.md#reference-ed53106ee50442d7a2dd3e1f60e6f0f8), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a), [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [색상 관리](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
