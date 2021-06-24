---
description: 이미지 집합. req=set 응답을 생성하는 데 사용할 이미지 세트 값을 지정합니다.
solution: Experience Manager
title: imageSet
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 318c658d-7126-40f6-870b-11294a3f6f5f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 8%

---

# imageSet{#imageset}

이미지 집합. req=set 응답을 생성하는 데 사용할 이미지 세트 값을 지정합니다.

`imageSet=val`

<table id="simpletable_F697691D166C407D82233664814F4663"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>이미지 세트 문자열입니다. </p></td> 
 </tr> 
</table>

값을 이스케이프 처리하고 포함된 모든 수정자가 URL 쿼리 문자열의 일부로 해석되지 않도록 하려면 전체 값을 중괄호로 묶어야 합니다. 카탈로그 레코드가 네트 경로에 지정된 경우 이 수정자 값은 기본 레코드의 `catalog::ImageSet`을 무시합니다. 유효한 이미지 세트 구문에 대한 설명은 `catalog::ImageSet` 설명서를 참조하십시오.

## 속성 {#section-66e7bb7bf4664cbcac6f7ebb2f0d3a4f}

요청 속성입니다. 선택 사항입니다. 기본 레코드에서 `catalog::ImageSet`을(를) 무시합니다.

## 기본값 {#section-e8622ff40408450fb79d028f8d37fa6b}

없음.

## 예 {#section-68513d3c601f477399602a0741dab390}

`req=set` 요청에 사용할 이미지 세트를 지정합니다.

`http://server/myRootId?imageSet={asset1,asset2,asset3}&req=set`

## 참조 {#section-7e0320b2e09d475897082711a8f023a9}

[catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md) ,  [req=set](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76),  [미디어 세트 요청](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-media-set-requests.md#reference-f2f2aa11208b47609fe17848d3b86a0b)
