---
description: 이미지 제공 기능은 특정 레코드에 대한 카탈로그 ImageSet과 연관된 모든 리소스 및 메타데이터를 나타내는 계층적 텍스트 응답(xml 또는 json)을 가져오는 메커니즘을 제공합니다.
solution: Experience Manager
title: 미디어 집합 요청
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71efed33-6248-4d23-ab4e-2caec3449171
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '957'
ht-degree: 0%

---

# 미디어 집합 요청{#media-set-requests}

이미지 제공 기능은 특정 레코드에 대해 카탈로그와 연관된 모든 리소스 및 메타데이터를 나타내는 계층적 텍스트 응답(xml 또는 json)을 가져오는 메커니즘을 제공합니다.

뷰어는 이 메커니즘을 사용하여 간단한 이미지, 비디오, 비디오 세트, 견본 세트, 스핀 세트, 페이지 세트(e-catalog) 및 미디어 세트를 보여주는 응답을 생성할 수 있습니다.

## 요청 구문 {#section-d72b1d95e4ce4bb1b332ce096c2b99f1}

에 대한 설정 응답 `catalog::ImageSet` 는 `req=set` 수정자 및 네트 경로에서 카탈로그 레코드 id 참조. 또는 를 사용하여 URL에서 직접 이미지 세트를 지정할 수 있습니다 `imageset=` 수정자. 만약 `imageset=` 수정자 는 이미지 집합을 지정하는 데 사용되며, 이미지 세트 값을 이스케이프하고 포함된 수정자가 URL 쿼리 문자열의 일부로 해석되지 않도록 하려면 전체 값을 중괄호로 묶어야 합니다.

## 설정된 응답 유형 {#section-93eb0a1f70344da2a888e56372ad3896}

설정 메커니즘은 다음과 같은 유형의 응답을 지원합니다.

<table id="simpletable_3718A93699F64805A41BC8A24D7962D2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>단순 이미지 </p></td> 
  <td class="stentry"> <p>없는 이미지 레코드 <span class="codeph"> 카탈로그::ImageSet</span> 정의됩니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>간단한 비디오 </p></td> 
  <td class="stentry"> <p>정적 컨텐츠 카탈로그의 비디오 레코드입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>견본 집합 </p></td> 
  <td class="stentry"> <p>이미지 레코드에 대한 참조와 견본으로 사용되는 이미지 레코드에 대한 선택적 별도 참조로 구성된 항목 집합입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>계층 견본 집합 </p></td> 
  <td class="stentry"> <p>기본 견본 항목이나 견본 집합 레코드에 대한 참조로 구성된 항목 집합입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>스핀 세트 </p></td> 
  <td class="stentry"> <p>단순 이미지 ID 목록으로 구성된 항목 세트입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2차원 스핀 세트 </p></td> 
  <td class="stentry"> <p>단순 이미지 또는 기본 스핀 세트에 대한 참조로 구성된 항목 집합입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>페이지 세트 </p></td> 
  <td class="stentry"> <p>최대 3개의 페이지 이미지 목록으로 구성된 항목 세트 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>미디어 집합 </p></td> 
  <td class="stentry"> <p>단순 이미지, 비디오 세트, 견본 세트, 계층 구조 견본 세트, 스핀 세트, 2차원 스핀 세트, 페이지 세트 및 비디오 자산으로 구성된 항목 세트입니다. 각 미디어 세트 항목에는 선택적 색상 견본을 포함할 수도 있습니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>비디오 세트 </p></td> 
  <td class="stentry"> <p>단순 비디오 목록으로 구성된 항목 세트입니다. </p></td> 
 </tr> 
</table>

## 외부 집합 형식 감지 {#section-3dd6e453528d46898e559d31458a59ba}

다음 경우에 `req=set` 요청이 수신되면 생성할 응답 유형은 의 값에 의해 결정됩니다. `catalog::AssetType`. If `catalog::AssetType` 가 정의되지 않은 경우 응답 유형은 다음 규칙에 의해 결정됩니다.

* 이미지 카탈로그에 레코드가 있으면 AND `catalog::ImageSet` 정의된 횟수

   * 레코드 Imageset 필드에 하나 이상의 항목이 콜론을 포함하는 경우 e-catalog 세트를 가정하십시오.
   * 레코드 이미지 집합 필드에 있는 하나 이상의 항목에 세미콜론이 두 개 있는 경우 미디어 집합을 가정합니다.
   * 레코드 Imageset 필드에 있는 하나 이상의 항목에 세미콜론이 하나 들어 있을 경우 이미지 세트를 가정해 보십시오.
   * 세미콜론과 세미콜론을 포함하는 항목이 없지만 하나 이상의 항목에 참조된 집합 또는 인라인 세트(2D 스핀 세트)가 포함되어 있는 경우 스핀 세트를 가정합니다.
   * 콜론 또는 세미콜론을 포함하는 항목이 없거나 참조된 세트 또는 인라인 세트(즉, 쉼표로 구분된 이미지 목록)를 포함하는 항목이 없으면 알 수 없는 설정이라고 가정합니다.

* 이미지 및 정적 컨텐츠 카탈로그 모두에 레코드가 있는 경우

   * 파일 확장자가 다음 세트에 있는 경우 비디오를 가정하십시오. mp3, mp4, flv, f4v, swf, xml
   * 이미지 제외

* 정적 콘텐츠 카탈로그에 레코드가 있지만 이미지 카탈로그에는 없는 경우

   * 파일 확장자가 다음 세트에 있는 경우 비디오를 가정하십시오. mp3, mp4, flv, f4v, swf, xml
   * 그렇지 않으면 정적 가정함

* 이미지 카탈로그에서 의 레코드가 있지만 정적 콘텐츠 카탈로그에는 없는 경우

   * 이미지 가정

* 이미지 카탈로그에서 레코드가 없고 정적 컨텐츠 카탈로그에서 찾을 수 없는 경우

   * 파일 확장자가 다음 세트에 있는 경우 파일 기반 비디오를 가정하십시오. mp3, mp4, flv, f4v, swf, xml
   * 그렇지 않으면 파일 기반 이미지를 가정합니다

모든 경우 결과 xml 응답은 감지된 유형에 해당하는 설정된 루트 노드가 있는 지정된 XML 문서를 따릅니다.

## 내부 집합 유형 감지 {#section-8f46490e467247e69ce284704def06f3}

외부 세트가 유형 미디어 세트로 감지되면 응답에는 의 각 미디어 세트 항목에 해당하는 미디어 세트 항목 세트가 포함됩니다 `catalog::ImageSet`. 선택적 유형 매개 변수가 특정 미디어 세트 항목에 대해 지정된 경우 다음 표에 따라 출력 유형에 매핑됩니다.

| 입력 유형 | 출력 유형 |
|---|---|
| `img` | `img` |
| `basic` | `img` |
| `advanced_image` | `img` |
| `img_set` | `img_set` |
| `advanced_image_set` | `img_set` |
| `advanced_swatchset` | `img_set` |
| `spin` | `spin` |
| `video` | `video` |
| `video_set` | `video_set` |
| `static` | `static` |
| `ecat` | `ecat` |

특정 미디어 세트 항목에 대한 선택적 유형 매개 변수를 지정하지 않았거나 지원되지 않는 유형에 해당하는 경우, 미디어 세트 항목 유형은 외부 세트 수준에서 적용된 것과 동일한 규칙을 사용하여 자동으로 검색됩니다.

## XML 사양 {#section-c1bd60948ef545759a16885bb6fcc607}

반환된 xml 응답은 다음 사양을 따릅니다.

`http://crc.scene7.com/is-docs/examples/mediaset.dtd`

## LabelKey {#section-bf565de6f7294cf89620343c9071f415}

다음 `labelkey=` 수정자는 와 함께 사용됩니다 `catalog::UserData`이미지 및 색상 견본의 레이블을 생성하는 필드입니다. 다음 `catalog:UserData` 필드는 키/값 쌍 세트로 구문 분석되고 이 세트에 있는 레이블 키 색인은 지정된 키에 대한 값을 검색합니다. 그런 다음 이 값은 *`l`* 에 대한 속성 *`s`* 및 *`i`*.

## 강제 제한 {#section-b9f042873bee45a5ae11b69fd42f2bca}

응답 크기를 제한하고 자체 참조 문제를 방지하기 위해 서버 속성에 의해 최대 중첩 깊이가 제어됩니다 `PS::fvctx.nestingLimit`. 이 제한을 초과하면 오류가 반환됩니다.

대형 전자 카탈로그 세트에 대한 xml 응답 크기를 제한하기 위해, 서버 속성에 따라 브로셔 세트 항목에 대한 비공개 메타데이터가 표시되지 않습니다 `PS::fvctx.brochureLimit`. 브로셔와 관련된 모든 비공개 메타데이터는 브로셔의 제한에 도달할 때까지 내보내집니다. 한도를 초과하면 개인 맵 및 사용자 데이터가 억제되고 해당 플래그가 억제된 데이터 유형을 나타내는 것으로 설정됩니다.

중첩된 미디어 세트는 지원되지 않습니다. 중첩된 미디어 세트는 미디어 세트 유형의 미디어 세트 항목을 포함하는 미디어 세트로 정의됩니다. 이 조건이 감지되면 오류가 반환됩니다.

## 예제 {#section-588c9d33aa05482c86cd2b1936887228}

에 대한 샘플 XML 응답 `req=set` 요청을 보려면 HTML 예 헤더 아래의 속성 페이지를 참조하십시오.

`http://crc.scene7.com/is-docs/examples/properties.htm`

## 참조 {#section-625ec466c948476e800dc0c52a4532d3}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) , [imageset=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3), [카탈로그::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [이미지 카탈로그 참조](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
