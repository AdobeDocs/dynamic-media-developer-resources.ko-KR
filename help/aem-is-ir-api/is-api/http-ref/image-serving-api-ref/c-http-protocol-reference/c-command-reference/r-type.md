---
title: 유형
description: 정적 콘텐츠 유형 필터입니다. /is/content를 통해 제공되는 정적 콘텐츠의 필터 문자열을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9015d5f4-e42c-43e0-af85-fc9c278448e7
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 4%

---

# 유형{#type}

정적 콘텐츠 유형 필터입니다. /is/content를 통해 제공되는 정적 콘텐츠의 필터 문자열을 지정합니다.

`type= *`val`*`

<table id="simpletable_B66354A826434A678F3DBC686A0F1436"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>필터 문자열을 입력합니다. </p></td> 
 </tr> 
</table>

서버는 값을 값과 비교합니다. `catalog::Type` 요청된 정적 콘텐츠 항목의 을 참조하십시오. 값이 일치하면(대/소문자 구분) 항목이 클라이언트에 반환되고, 그렇지 않으면 오류가 반환됩니다.

## 속성 {#section-529b088434a44a9f86a64ef548d2925b}

를 통해 제공되는 정적 콘텐츠(이미지가 아닌) 요청에 대해서만 지원됩니다. 다음과 같은 경우 무시됨 `catalog::Type` 은(는) 비어 있거나 정의되지 않았습니다.

## 기본값 {#section-e9e8f51d0a01452183ccb510efd87d46}

다음과 같은 경우 유형 일치가 적용되지 않습니다. `type=` 이(가) 지정되지 않았거나 비어 있습니다.

## 참조 {#section-da60777a46a74f1bbfa5b2f3b240eb0f}

[정적(이미지가 아닌) 콘텐츠 제공](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-serving-static-non-image-content.md#reference-cbe50e697fdf4c7bbb0084f98b7739da), [catalog:::UserType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-usertype-cat.md)
