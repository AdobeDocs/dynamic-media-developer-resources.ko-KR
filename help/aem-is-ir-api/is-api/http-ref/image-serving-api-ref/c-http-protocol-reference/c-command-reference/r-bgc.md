---
description: 배경색 보기를 참조하십시오. 합성 이미지(이미지 보기)의 배경색을 지정합니다.
seo-description: 배경색 보기를 참조하십시오. 합성 이미지(이미지 보기)의 배경색을 지정합니다.
seo-title: bgc
solution: Experience Manager
title: bgc
topic: Scene7 Image Serving - Image Rendering API
uuid: 3ea8291e-3223-45ff-a2ad-43fc212eff90
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# bgc{#bgc}

배경색 보기를 참조하십시오. 합성 이미지(이미지 보기)의 배경색을 지정합니다.

`bgc= *`color`*`

<table id="simpletable_998CF426296945FEA48D19E33B71A17E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 색상</span></span> </p> </td> 
  <td class="stentry"> <p>회색, RGB 또는 CMYK 색상 값입니다. </p></td> 
 </tr> 
</table>

보기 배경에 사용할 불투명한 채우기 색상을 지정합니다. 합성 이미지에 투명한 영역이 있거나 합성 이미지에 보기 사각형과 다른 종횡비가 있는 경우에만 표시됩니다. 또는 인 경우 `fmt=tif-alpha` 또는 `fmt=png-alpha`또는 `req=mask`를 무시합니다.

>[!NOTE]
>
>&#39;s&#39; 색상 접미사는 에 의해 무시됩니다 `bgc=`. 로 지정된 색상 값은 `bgc=` 항상 해당 출력 색상 공간과 연결됩니다.

## 속성 {#section-b729b50b1ea7433b82ba34ecd61839cd}

속성을 봅니다. 현재 레이어 설정에 관계없이 적용됩니다. if, `req=mask`, `fmt=tif-alpha``fmt=png-alpha`, `fmt=gif-alpha`or `fmt=swf-alpha`은 무시됩니다.

색상으로 지정된 모든 알파 값은 무시됩니다.

*`color`* 는 출력 색상 공간(에 지정된 대로)에 속하며 출력 이미지와 동일한 픽셀 유형을 `icc=`가져야 합니다. 픽셀 유형이 일치하지 않으면 *`color`* 잘못 변환하여 변환됩니다.

## 기본값 {#section-4e025cbd723547b5ab4450f7aad70da3}

`attribute::BkgColor`.

## 예 {#section-7bcdfbc0e1274e86a69d39186b090789}

축소판 요청에 대한 명시적 배경색을 지정합니다.

`http://server/myRootId/myImageId?req=tmb&bgc=214,245,130`

## 참조 {#section-1e55f9f98f1847918a1725836a27cfaa}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93)attribute::KgColor [,](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-bkgcolor.md#reference-ed53106ee50442d7a2dd3e1f60e6f0f8)fmt=req, [ective=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)req, [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)[, Color Management](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
