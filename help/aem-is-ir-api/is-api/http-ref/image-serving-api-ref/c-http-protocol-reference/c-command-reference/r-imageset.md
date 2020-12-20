---
description: 이미지 집합. req=set 응답을 생성할 때 사용할 이미지 집합 값을 지정합니다.
seo-description: 이미지 집합. req=set 응답을 생성할 때 사용할 이미지 집합 값을 지정합니다.
seo-title: imageSet
solution: Experience Manager
title: imageSet
topic: Scene7 Image Serving - Image Rendering API
uuid: ecfb3905-e3ef-4ab8-a2c4-2c3f200e0f0f
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 9%

---


# imageSet{#imageset}

이미지 집합. req=set 응답을 생성할 때 사용할 이미지 집합 값을 지정합니다.

`imageSet=val`

<table id="simpletable_F697691D166C407D82233664814F4663"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>이미지 집합 문자열. </p></td> 
 </tr> 
</table>

값을 escape하고 포함된 수정자가 URL 쿼리 문자열의 일부로 해석되지 않도록 하려면 전체 값을 중괄호로 묶어야 합니다. 카탈로그 레코드가 순경로에 지정된 경우 이 수정자 값은 기본 레코드의 `catalog::ImageSet`을 무시합니다. 유효한 이미지 집합 구문에 대한 설명은 `catalog::ImageSet` 설명서를 참조하십시오.

## 속성 {#section-66e7bb7bf4664cbcac6f7ebb2f0d3a4f}

요청 속성을 참조하십시오. 선택 사항입니다. 기본 레코드의 `catalog::ImageSet`을(를) 재정의합니다.

## 기본값 {#section-e8622ff40408450fb79d028f8d37fa6b}

없음.

## 예 {#section-68513d3c601f477399602a0741dab390}

`req=set` 요청에 사용할 이미지 세트를 지정합니다.

`http://server/myRootId?imageSet={asset1,asset2,asset3}&req=set`

## 참조 {#section-7e0320b2e09d475897082711a8f023a9}

[카탈로그::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md) ,  [req=set](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76),  [미디어 집합 요청](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-media-set-requests.md#reference-f2f2aa11208b47609fe17848d3b86a0b)
