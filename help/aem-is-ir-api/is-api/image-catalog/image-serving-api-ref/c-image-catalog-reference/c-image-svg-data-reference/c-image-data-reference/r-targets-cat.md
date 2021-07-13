---
description: 대상 데이터 확대/축소. 확대/축소 대상 속성이 없음 또는 그 이상이며 확대/축소 뷰어 클라이언트와 함께 사용할 수 있습니다.
solution: Experience Manager
title: 목표
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b882ba01-a1ef-4179-95c7-964c2578aad1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 2%

---

# 목표{#targets}

대상 데이터 확대/축소. 확대/축소 대상 속성이 없음 또는 그 이상이며 확대/축소 뷰어 클라이언트와 함께 사용할 수 있습니다.

서버는 &#39; `??`&#39; 레코드 종결자 토큰을 바꾼 후 `req=targets`에 대한 응답으로 이 필드의 콘텐츠를 반환합니다.

최대 4개의 속성을 각 확대/축소 대상과 연결할 수 있습니다.

` Target. *``*.frame= *`numframe`*`

` Target. *``*.rect= *`numleft,top,width,height`*`

` Target. *``*.label= *`numlabel`*`

` Target. *``*.userData= *`numuserData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> num  </span> </span> </p> </td> 
  <td class="stentry"> <p>대상 번호 확대/축소(int); 확대/축소 타겟은 1부터 순차적으로 연속적으로 번호가 매겨야 합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 프레임  </span> </span> </p> </td> 
  <td class="stentry"> <p>스핀 또는 브로셔 세트의 특정 프레임/페이지를 타깃팅하는 선택적 프레임/페이지 번호 스핀 및 브로셔 뷰어를 사용하도록 지정하지 않으면 기본값이 0으로 설정됩니다. 확대/축소 뷰어에서 무시됨. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 왼쪽, 위쪽  </span> </span> </p> </td> 
  <td class="stentry"> <p>이미지의 왼쪽 위에서 확대/축소 대상 사각형의 왼쪽 상단까지 픽셀 오프셋(int, int); 0보다 커야 합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 너비, 높이  </span> </span> </p> </td> 
  <td class="stentry"> <p>확대/축소 대상 사각형의 픽셀 크기(int, int); 0보다 커야 합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 레이블  </span> </span> </p> </td> 
  <td class="stentry"> <p>텍스트 데이터 값; 확대/축소 대상 링크의 텍스트 레이블로 사용될 수 있습니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> userData  </span> </span> </p> </td> 
  <td class="stentry"> <p>텍스트 데이터 값; 는 SKU 값 또는 핫 링크 URL과 같은 대상에 대한 정보를 클라이언트에 전달하는 데 사용할 수 있습니다. </p> </td> 
 </tr> 
</table>

목표. *`num`*.rect는 각 확대/축소 대상에 필요하며 이미지 내에 사각형을 완전히 지정해야 합니다. 다른 모든 속성은 선택 사항입니다.

*`label`* 텍스트 문자열 현지화에  *`userData`* 참여합니다. 자세한 내용은 *HTTP 프로토콜 참조*&#x200B;에서 [텍스트 문자열 현지화](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) 를 참조하십시오.

스핀 뷰어 및 브로셔 뷰어 클라이언트와 관련된 애플리케이션의 경우 확대/축소 타겟은 이미지 세트를 정의하는 동일한 카탈로그 레코드에서 정의해야 합니다. 이미지 집합 구성원의 카탈로그 레코드에 있는 확대/축소 대상 정의는 뷰어에서 무시됩니다.

Dynamic Media 뷰어는 `catalog::Modifier`의 명령에 의해 이미 조정된 전체 해상도 이미지의 좌표에서 확대/축소 타겟을 예상합니다.

## 속성 {#section-b3f8eba4985f4b00bb935d592fe770f9}

[속성 ](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) 데이터 값.

## 기본값 {#section-feab29f6575e482391086a57f547543c}

없음.

## 참조 {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[catalog::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) ,  [catalog::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834),  [req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md),  [텍스트 문자열 현지화](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
