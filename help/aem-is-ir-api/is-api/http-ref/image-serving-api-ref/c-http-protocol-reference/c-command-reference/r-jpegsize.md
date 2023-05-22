---
description: Jpeg 크기(킬로 바이트). JPEG 응답의 최대 크기(KB)를 지정합니다.
solution: Experience Manager
title: jpeg 크기
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08cecb09-100f-4671-b335-d59c88b0e1ef
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 3%

---

# jpeg 크기{#jpegsize}

Jpeg 크기(킬로 바이트). JPEG 응답의 최대 크기(KB)를 지정합니다.

`jpegSize= *`크기`*`

<table id="simpletable_EC2A8D8B65854B45B9CB184DA1069355"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 크기</span></span> </p> </td> 
  <td class="stentry"> <p>크기(KB)입니다. </p></td> 
 </tr> 
</table>

이 값이 양의 값으로 설정되고 지정된 JPEG 품질의 JPEG 응답이 이 값을 초과하지 않으면 해당 이미지가 응답으로서 반환됩니다. 그렇지 않으면 지정된 크기에 맞는 이미지를 생성하거나 이미지가 맞지 않는다고 판단될 때까지 JPEG 품질이 저하됩니다. 후자의 경우 오류로 인해 요청이 실패합니다.

값이 0이면 응답이 크기에 의해 제한되지 않음을 의미합니다.

음수 값은 허용되지 않습니다.

## 속성 {#section-19e544e77d35478b98fe8666f27d6968}

요청 속성입니다. 현재 레이어 설정에 관계없이 적용됩니다. 출력 이미지 형식이 JPEG 형식이 아니면 무시됩니다.

## 기본값 {#section-198b798ed187453197e0969c641d6fb5}

0

## 예 {#section-46bf806fd3ef4875b7726df32b6f834d}

보장 크기는 메모리가 제한된 장치로 전달하는 데 너무 크지 않습니다.

`http://server/myRoodId/myImageId?qlt=60&wid=300&jpegSize=10`

## 참조 {#section-98d472b39d6547969fce6dd86748c153}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [attribute::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
