---
description: 대상 데이터 확대/축소 확대/축소 대상 속성이 없습니다. 확대/축소 뷰어 클라이언트와 함께 사용할 수 있습니다.
seo-description: 대상 데이터 확대/축소 확대/축소 대상 속성이 없습니다. 확대/축소 뷰어 클라이언트와 함께 사용할 수 있습니다.
seo-title: 목표
solution: Experience Manager
title: 목표
topic: Scene7 Image Serving - Image Rendering API
uuid: ca02483a-9aa0-4b54-b6f0-4fd10d8b2b4c
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710

---


# 목표{#targets}

대상 데이터 확대/축소 확대/축소 대상 속성이 없습니다. 확대/축소 뷰어 클라이언트와 함께 사용할 수 있습니다.

서버는 &#39; 레코드 종결자 토큰을 교체한 `req=targets`후, 에 대한 응답으로 이 필드의 `??`내용을 반환합니다.

최대 4개의 속성이 각 확대/축소 대상과 연결될 수 있습니다.

` Target. *``*.frame= *`숫자 프레임`*`

` Target. *``*.rect= *`numleft,top,width,height`*`

` Target. *``*.label= *`숫자 레이블`*`

` Target. *``*.userData= *`numuserData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 숫자 </span></span> </p> </td> 
  <td class="stentry"> <p>확대/축소 대상 번호(int);확대/축소 타겟은 1부터 순차적으로 그리고 연속적으로 번호가 매겨져야 합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 프레임 </span></span> </p> </td> 
  <td class="stentry"> <p>스핀 또는 브로셔 세트의 특정 프레임/페이지를 타깃팅하기 위한 선택적 프레임/페이지 번호회전 및 브로셔 뷰어에 대해 지정되지 않은 경우 기본값은 0입니다.확대/축소 뷰어에 의해 무시됩니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 왼쪽, 위쪽 <span class="varname"> </span></span> </p> </td> 
  <td class="stentry"> <p>이미지의 왼쪽 위에서 확대/축소 대상 사각형의 왼쪽 위(int, int)까지 픽셀 오프셋;은 0보다 커야 합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 너비, 높이 <span class="varname"> </span></span> </p> </td> 
  <td class="stentry"> <p>확대/축소 대상 사각형의 픽셀 크기(int, int);은 0보다 커야 합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 레이블 </span></span> </p> </td> 
  <td class="stentry"> <p>텍스트 데이터 값;확대/축소 대상 링크에 대한 텍스트 레이블로 사용할 수 있습니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 사용자 <span class="varname"> 데이터 </span></span> </p> </td> 
  <td class="stentry"> <p>텍스트 데이터 값;은 SKU 값 또는 핫 링크 URL과 같은 타겟 특정 정보를 클라이언트에 전달하는 데 사용될 수 있습니다. </p> </td> 
 </tr> 
</table>

목표. *`num`*.rect는 각 확대/축소 대상에 필요하며 이미지 내에서 사각형을 완전히 지정해야 합니다. 다른 모든 속성은 선택 사항입니다.

*`label`* 텍스트 문자열 현지화에 *`userData`* 참여하십시오. 자세한 내용은 [HTTP 프로토콜](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) 참조 *문서의 텍스트 문자열 현지화를* 참조하십시오.

스핀 뷰어 및 브로셔 뷰어 클라이언트가 포함된 응용 프로그램의 경우, 확대/축소 타겟은 이미지 세트를 정의하는 동일한 카탈로그 레코드에서 정의되어야 합니다. 뷰어에서 이미지 세트 구성원의 카탈로그 레코드에 있는 모든 확대/축소 대상 정의는 무시됩니다.

Scene7 뷰어에서는 명령을 통해 이미 조정된 전체 해상도 이미지의 좌표에서 확대/축소 타겟을 예상할 수 `catalog::Modifier`있습니다.

## 속성 {#section-b3f8eba4985f4b00bb935d592fe770f9}

[속성 데이터](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) 값.

## 기본값 {#section-feab29f6575e482391086a57f547543c}

없음.

## 참조 {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[catalog::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) , [catalog::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834), [req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [Text StringLocalization](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
