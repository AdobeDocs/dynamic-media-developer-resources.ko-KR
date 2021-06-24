---
description: 정적 콘텐츠 유형 필터입니다. /is/content를 통해 전달된 정적 콘텐츠의 필터 문자열을 지정합니다.
solution: Experience Manager
title: 유형
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 9015d5f4-e42c-43e0-af85-fc9c278448e7
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 5%

---

# 유형{#type}

정적 콘텐츠 유형 필터입니다. /is/content를 통해 전달된 정적 콘텐츠의 필터 문자열을 지정합니다.

`type= *`val`*`

<table id="simpletable_B66354A826434A678F3DBC686A0F1436"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>필터 문자열을 입력합니다. </p></td> 
 </tr> 
</table>

서버는 val을 요청된 정적 콘텐츠 항목의 `catalog::Type` 값과 비교합니다. 값이 일치하면(대/소문자 구분) 항목이 클라이언트에 반환되고, 그렇지 않으면 오류가 반환됩니다.

## 속성 {#section-529b088434a44a9f86a64ef548d2925b}

를 통해 제공되는 정적 콘텐츠(비이미지) 요청에만 지원됩니다. `catalog::Type`이 비어 있거나 정의되어 있지 않으면 무시됩니다.

## 기본값 {#section-e9e8f51d0a01452183ccb510efd87d46}

`type=` 이 지정되지 않았거나 비어 있는 경우 유형 일치가 적용되지 않습니다.

## 참조 {#section-da60777a46a74f1bbfa5b2f3b240eb0f}

[정적(비이미지) 콘텐츠 제공](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-serving-static-non-image-content.md#reference-cbe50e697fdf4c7bbb0084f98b7739da),  [카탈로그::UserType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-usertype-cat.md)
