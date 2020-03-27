---
description: 이미지 제공은 특정 레코드에 대한 카탈로그 ImageSet과 연결된 모든 리소스 및 메타데이터를 나타내는 계층 텍스트 응답(xml 또는 json)을 가져오기 위한 메커니즘을 제공합니다.
seo-description: 이미지 제공은 특정 레코드에 대한 카탈로그 ImageSet과 연결된 모든 리소스 및 메타데이터를 나타내는 계층 텍스트 응답(xml 또는 json)을 가져오기 위한 메커니즘을 제공합니다.
seo-title: 미디어 집합 요청
solution: Experience Manager
title: 미디어 집합 요청
topic: Scene7 Image Serving - Image Rendering API
uuid: af9fabcd-531d-43fb-bd97-269923bea5e8
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# 미디어 집합 요청{#media-set-requests}

이미지 제공은 특정 레코드에 대해 catalog::ImageSet과 연결된 모든 리소스 및 메타데이터를 나타내는 계층 텍스트 응답(xml 또는 json)을 가져오기 위한 메커니즘을 제공합니다.

뷰어는 이 메커니즘을 사용하여 간단한 이미지, 비디오, 비디오 세트, 견본 세트, 스핀 세트, 페이지 세트(e카탈로그) 및 미디어 세트를 표시하는 응답을 생성할 수 있습니다.

## 요청 구문 {#section-d72b1d95e4ce4bb1b332ce096c2b99f1}

수정자를 사용하고 순 경로에서 카탈로그 레코드 ID를 참조하면 에 대한 세트 응답을 검색할 `catalog::ImageSet` `req=set` 수 있습니다. 또는 `imageset=` 수정자를 사용하여 URL에서 직접 이미지 세트를 지정할 수 있습니다. 수정자가 이미지 집합을 지정하는 데 사용되는 경우 이미지 집합 값을 escape하고 포함된 수정자가 URL 쿼리 문자열의 일부로 해석되지 않도록 하기 위해 전체 값을 중괄호로 묶어야 합니다. `imageset=`

## 설정된 응답 유형 {#section-93eb0a1f70344da2a888e56372ad3896}

설정 메커니즘은 다음 유형의 응답을 지원합니다.

<table id="simpletable_3718A93699F64805A41BC8A24D7962D2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>간단한 이미지 </p></td> 
  <td class="stentry"> <p>카탈로그 없는 <span class="codeph"> 이미지 레코드::ImageSet</span> 정의 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>간단한 비디오 </p></td> 
  <td class="stentry"> <p>정적 컨텐츠 카탈로그의 비디오 레코드입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>견본 집합 </p></td> 
  <td class="stentry"> <p>이미지 레코드에 대한 참조와 견본으로 사용되는 이미지 레코드에 대한 선택적 개별 참조로 구성된 항목 집합. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>계층적 견본 집합 </p></td> 
  <td class="stentry"> <p>기본 견본 항목 또는 견본 집합 레코드에 대한 참조로 구성된 항목 집합. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>스핀 세트 </p></td> 
  <td class="stentry"> <p>간단한 이미지 ID 목록으로 구성된 항목 집합. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2차원 회전 집합 </p></td> 
  <td class="stentry"> <p>간단한 이미지 또는 기본 회전 집합에 대한 참조로 구성된 항목 집합. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>페이지 세트 </p></td> 
  <td class="stentry"> <p>최대 3개의 페이지 이미지 목록으로 구성된 항목 집합 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>미디어 세트 </p></td> 
  <td class="stentry"> <p>단순 이미지, 비디오 세트, 견본 세트, 계층 견본 집합, 스핀 집합, 2차원 스핀 집합, 페이지 집합 및 비디오 에셋으로 구성된 항목 집합. 각 미디어 세트 항목에는 선택 사항 견본도 포함될 수 있습니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>비디오 세트 </p></td> 
  <td class="stentry"> <p>간단한 비디오 목록으로 구성된 항목 집합. </p></td> 
 </tr> 
</table>

## 외부 집합 유형 감지 {#section-3dd6e453528d46898e559d31458a59ba}

요청이 `req=set` 수신되면 생성할 응답 유형은 의 값에 의해 결정됩니다 `catalog::AssetType`. 을 `catalog::AssetType` 정의하지 않으면 다음 규칙에 따라 응답 유형이 결정됩니다.

* 이미지 카탈로그에서 레코드가 발견되고 AND가 `catalog::ImageSet` 정의된 경우

   * 레코드 이미지 집합 필드에 콜론이 하나 이상 들어 있는 경우 전자 카탈로그 집합을 가정합니다.
   * 레코드 이미지 집합 필드에 있는 하나 이상의 항목에 두 개의 세미콜론이 포함된 경우 미디어 집합을 가정해 보십시오.
   * 레코드 이미지 집합 필드에 세미콜론이 하나 이상 들어 있는 경우 이미지 집합을 가정해 보십시오.
   * 항목에 콜론과 세미콜론이 없지만 하나 이상의 항목에 참조된 집합 또는 인라인 집합이 포함되어 있는 경우 회전 집합을 가정해 보십시오(이것은 2D 회전 집합).
   * 콜론이나 세미콜론을 포함하는 항목이 없거나 참조된 집합 또는 인라인 집합(즉, 쉼표로 구분된 이미지 목록)이 없는 경우 알 수 없는 집합으로 간주합니다.

* 이미지 AND 정적 컨텐츠 카탈로그에 레코드가 있는 경우

   * 파일 확장자가 다음 집합에 있으면 비디오를 가정해 보십시오.mp3, mp4, flv, f4v, swf, xml
   * 그렇지 않은 경우 이미지 가정

* 정적 컨텐츠 카탈로그에 레코드가 있지만 이미지 카탈로그에는 없는 경우

   * 파일 확장자가 다음 집합에 있으면 비디오를 가정해 보십시오.mp3, mp4, flv, f4v, swf, xml
   * 정적인 경우를 가정해 보십시오

* 이미지 카탈로그에 있는 레코드가 있지만 정적 컨텐츠 카탈로그에 없는 경우

   * 이미지 추정

* 이미지 카탈로그에서 레코드가 없고 정적 컨텐츠 카탈로그에 없는 경우

   * 파일 확장자가 다음 세트에 있는 경우 파일 기반 비디오를 가정해 보십시오.mp3, mp4, flv, f4v, swf, xml
   * 파일 기반 이미지를 가정할 경우

모든 경우 결과 xml 응답은 감지된 유형에 해당하는 세트 루트 노드가 있는 지정된 XML 문서를 준수합니다.

## 내부 세트 유형 감지 {#section-8f46490e467247e69ce284704def06f3}

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

특정 미디어 세트 항목에 대한 선택적 유형 매개 변수가 지정되지 않았거나 지원되지 않는 유형에 해당하는 경우, 미디어 세트 항목 유형은 외부 세트 수준에서 적용된 것과 동일한 규칙을 사용하여 자동으로 검색됩니다.

## XML 사양 {#section-c1bd60948ef545759a16885bb6fcc607}

반환된 xml 응답은 다음 사양을 따릅니다.

`http://crc.scene7.com/is-docs/examples/mediaset.dtd`

## LabelKey {#section-bf565de6f7294cf89620343c9071f415}

수정자는 이미지 및 견본용 레이블을 생성하기 위해 `labelkey=` `catalog::UserData`필드와 함께 사용됩니다. 이 `catalog:UserData` 필드는 키/값 쌍의 집합으로 구문 분석되고 주어진 키에 대한 값을 검색하기 위해 이 세트에 대한 레이블 키 색인이 표시됩니다. 그런 다음 이 값은 and의 *`l`* 특성으로 *`s`* 반환됩니다 *`i`*.

## 강제 적용 제한 {#section-b9f042873bee45a5ae11b69fd42f2bca}

응답의 크기를 제한하고 자체 참조 문제를 방지하기 위해 서버 속성에 의해 최대 중첩 깊이가 제어됩니다 `PS::fvctx.nestingLimit`. 이 제한을 초과하면 오류가 반환됩니다.

큰 전자 카탈로그 집합에 대한 XML 응답 크기를 제한하기 위해 서버 속성에 따라 브로셔 세트 항목에 대한 비공개 메타데이터가 표시되지 않습니다 `PS::fvctx.brochureLimit`. 브로셔 제한에 도달할 때까지 브로셔와 연결된 모든 비공개 메타데이터를 내보냅니다. 제한이 초과되면 개인 맵과 사용자 데이터가 억제되고 해당 플래그가 억제된 데이터 유형을 표시하도록 설정됩니다.

중첩 미디어 세트는 지원되지 않습니다. 중첩 미디어 세트는 미디어 세트 유형의 미디어 세트 항목을 포함하는 미디어 세트로 정의됩니다. 이 조건이 감지되면 오류가 반환됩니다.

## 예제 {#section-588c9d33aa05482c86cd2b1936887228}

요청에 대한 샘플 XML 응답은 HTML 예제 헤더 아래의 속성 페이지를 참조하십시오. `req=set`

`http://crc.scene7.com/is-docs/examples/properties.htm`

## 참조 {#section-625ec466c948476e800dc0c52a4532d3}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) , [imageset=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3), [catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [Image Catalog Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)

