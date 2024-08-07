---
title: 이미지 집합
description: 이미지 집합. req=set 응답을 생성할 때 사용할 이미지 세트 값을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 318c658d-7126-40f6-870b-11294a3f6f5f
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 4%

---

# 이미지 집합{#imageset}

이미지 집합. req=set 응답을 생성할 때 사용할 이미지 세트 값을 지정합니다.

`imageSet=val`

<table id="simpletable_F697691D166C407D82233664814F4663"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 값</span></span> </p> </td> 
  <td class="stentry"> <p>이미지 집합 문자열입니다. </p></td> 
 </tr> 
</table>

값을 이스케이프 처리하고 포함된 수정자가 URL 쿼리 문자열의 일부로 해석되지 않도록 하려면 전체 값을 중괄호로 묶어야 합니다. 카탈로그 레코드가 네트 경로에 지정된 경우 이 한정자 값은 기본 레코드에서 `catalog::ImageSet`을(를) 재정의합니다. 올바른 이미지 집합 구문에 대한 설명은 `catalog::ImageSet` 설명서를 참조하십시오.

## 속성 {#section-66e7bb7bf4664cbcac6f7ebb2f0d3a4f}

요청 속성입니다. 선택 사항입니다. 기본 레코드에서 `catalog::ImageSet`을(를) 재정의합니다.

## 기본값 {#section-e8622ff40408450fb79d028f8d37fa6b}

없음.

## 예 {#section-68513d3c601f477399602a0741dab390}

`req=set` 요청에 사용할 이미지 집합을 지정하십시오.

`http://server/myRootId?imageSet={asset1,asset2,asset3}&req=set`

## 참조 {#section-7e0320b2e09d475897082711a8f023a9}

[카탈로그::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md) , [req=set](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [미디어 집합 요청](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-media-set-requests.md#reference-f2f2aa11208b47609fe17848d3b86a0b)
