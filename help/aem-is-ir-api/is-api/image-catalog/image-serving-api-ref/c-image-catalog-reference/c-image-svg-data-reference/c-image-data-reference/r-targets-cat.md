---
description: 대상 데이터를 확대/축소합니다. 확대/축소 대상 속성이 없습니다. 확대/축소 뷰어 클라이언트와 함께 사용할 수 있습니다.
seo-description: 대상 데이터를 확대/축소합니다. 확대/축소 대상 속성이 없습니다. 확대/축소 뷰어 클라이언트와 함께 사용할 수 있습니다.
seo-title: 목표
solution: Experience Manager
title: 목표
topic: Scene7 Image Serving - Image Rendering API
uuid: ca02483a-9aa0-4b54-b6f0-4fd10d8b2b4c
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 2%

---


# 목표{#targets}

대상 데이터를 확대/축소합니다. 확대/축소 대상 속성이 없습니다. 확대/축소 뷰어 클라이언트와 함께 사용할 수 있습니다.

서버는 &#39; `??`&#39; 레코드 종결자 토큰을 교체한 후 `req=targets`에 대한 응답으로 이 필드의 내용을 반환합니다.

각 확대/축소 대상과 최대 4개의 속성을 연결할 수 있습니다.

` Target. *``*.frame= *`키프레임`*`

` Target. *``*.rect= *`numleft,top,width,height`*`

` Target. *``*.label= *`숫자 레이블`*`

` Target. *``*.userData= *`numuserData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> num  </span> </span> </p> </td> 
  <td class="stentry"> <p>확대/축소 대상 번호(int);확대/축소 타겟은 1부터 순차적으로 그리고 연속적으로 번호가 매겨야 합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 프레임  </span> </span> </p> </td> 
  <td class="stentry"> <p>스핀 또는 브로셔 세트의 특정 프레임/페이지를 타깃팅하기 위한 선택적 프레임/페이지 번호회전 및 브로셔 뷰어 사용에 대해 지정되지 않은 경우 기본값은 0입니다.확대/축소 뷰어에서 무시됩니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 왼쪽, 위쪽  </span> </span> </p> </td> 
  <td class="stentry"> <p>이미지의 왼쪽 위에서 확대/축소 대상 사각형의 왼쪽 위(int, int)까지 픽셀 오프셋;0보다 커야 합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 너비, 높이  </span> </span> </p> </td> 
  <td class="stentry"> <p>확대/축소 대상 사각형의 픽셀 크기(int, int);은 0보다 커야 합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> label  </span> </span> </p> </td> 
  <td class="stentry"> <p>텍스트 데이터 값;확대/축소 대상 링크에 대한 텍스트 레이블로 사용할 수 있습니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> userData  </span> </span> </p> </td> 
  <td class="stentry"> <p>텍스트 데이터 값;는 SKU 값 또는 핫 링크 URL과 같은 대상 특정 정보를 클라이언트에 전달하는 데 사용할 수 있습니다. </p> </td> 
 </tr> 
</table>

목표. *`num`*.rect는 각 확대/축소 대상에 필요하며 이미지 내에서 사각형을 완전히 지정해야 합니다. 다른 모든 속성은 선택 사항입니다.

*`label`* 텍스트 문자열 현지화에  *`userData`* 참여할 수 있습니다. 자세한 내용은 *HTTP 프로토콜 참조*&#x200B;의 [텍스트 문자열 현지화](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)를 참조하십시오.

스핀 및 브로셔 뷰어 클라이언트가 포함된 응용 프로그램의 경우 확대/축소 타겟을 이미지 세트를 정의하는 동일한 카탈로그 레코드에 정의해야 합니다. 이미지 집합 구성원의 카탈로그 레코드에 있는 확대/축소 대상 정의는 뷰어에서 무시됩니다.

Scene7 뷰어는 `catalog::Modifier`의 명령으로 이미 조정된 전체 해상도 이미지의 좌표에 확대/축소 타겟이 있을 것으로 예상합니다.

## 속성 {#section-b3f8eba4985f4b00bb935d592fe770f9}

[속성 ](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) 데이터 값.

## 기본값 {#section-feab29f6575e482391086a57f547543c}

없음.

## 참조 {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[카탈로그::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) ,  [카탈로그::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834),  [req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md),  [텍스트 문자열 현지화](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
