---
description: 최종 보기 사각형. 최종 보기 이미지를 여러 조각이나 타일로 분해하여 클라이언트가 별도로 배달하고 다시 조합할 수 있으며 가장자리에 가공물이 없습니다.
seo-description: 최종 보기 사각형. 최종 보기 이미지를 여러 조각이나 타일로 분해하여 클라이언트가 별도로 배달하고 다시 조합할 수 있으며 가장자리에 가공물이 없습니다.
seo-title: rect
solution: Experience Manager
title: rect
topic: Scene7 Image Serving - Image Rendering API
uuid: c4830fc5-d102-4789-8753-0a660d4a557e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 1%

---


# rect{#rect}

최종 보기 사각형. 최종 보기 이미지를 여러 조각이나 타일로 분해하여 클라이언트가 별도로 배달하고 다시 조합할 수 있으며 가장자리에 가공물이 없습니다.

`rect= *``*, *``*[, *`Coordsizescale`*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>보기 이미지의 왼쪽 위 모서리에서 보기 사각형(int, int)의 왼쪽 위 모서리까지의 픽셀 오프셋은 <span class="varname"> scale</span> 이 적용된 후 픽셀로 표현됩니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 크기</span> </p></td> 
  <td class="stentry"> <p>ROI의 크기(픽셀 단위: int, int). 응답 이미지 크기를 지정합니다. 이미지가 보기 이미지로 간주되지 않는 영역(또는 <span class="codeph"> fmt=*-alpha</span>이 요청에 있는 경우 투명한 왼쪽)에 <span class="codeph"> bgc=</span>으로 채워집니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> scale</span> </p></td> 
  <td class="stentry"> <p>비율 인수(실제). 1.0보다 작은 값은 해상도를 줄이고 1.0보다 큰 값은 해상도를 높입니다. </p></td> 
 </tr> 
</table>

이 명령을 사용하면 이미지 제공 시 HTTP를 통해 큰 이미지를 전달할 수 있습니다. 그렇지 않으면 `attribute::MaxPix`으로 구성된 크기 제한을 초과할 수 있습니다.

>[!NOTE]
>
>JPEG 압축을 사용할 때 최상의 결과를 얻으려면 스트립 또는 타일 크기가 JPEG 인코딩 타일 크기(16x16픽셀)의 여러 배여야 합니다.

## 예 {#section-932fcfcb41d74a29bc929e4430c49601}

다운로드 파일 크기를 줄이기 위해 인쇄 가능한 CMYK 이미지를 여러 개의 전체 해상도 스트립으로 분리합니다. 인접한 이미지를 요청하려면 다음을 수행합니다.

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&fmt=tif&icc=WebCoated`

먼저 이미지에 대한 관련 정보를 얻습니다.

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&req=props`

텍스트 응답에는 다음과 같은 속성이 포함됩니다.

`image.width=2000 image.height=2400 image.version=37JK6NTvpvC42F5gOuLEVY`

이 정보를 바탕으로 600x2000픽셀 크기의 브러시를 4개 이상 선택합니다. `rect=` 명령은 스트립 크기 및 위치를 설명하는 데 사용됩니다.

이 이미지가 자주 변경되므로, CDN 또는 프록시 서버에 캐시되었을 수 있는 이전 버전의 이미지와 하나 이상의 스트립으로 끝날 가능성을 최소화하기 위해 `id=` 명령을 포함할 것입니다. `image.version` 속성 값이 이 용도로 사용됩니다.

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## 속성 {#section-aae223cee13e46d38b74680c048d945b}

속성을 봅니다. 현재 레이어 설정에 관계없이 적용됩니다.

보기 이미지 외부에 확장되는 ROI의 모든 영역은 `bgc=`으로 채워집니다.

`rect=`은(는) `scl=`, `wid=`, `hei=`, `fit=`, `rgn=` 및 `align=`과(와) 함께 *의 최종 크기 조절 및 맞춤이 적용됩니다.*

## 기본값 {#section-b296d3bbfb19441f87137a452b70f19a}

수정되지 않은 전체 보기 이미지( `rect=0,0,width,height,1.0`).

## 참조 {#section-74015202c0c545ec82aec614d74b4bbd}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) ,  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac),  [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47),  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f)  [ ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)  [,align=fit=,속성::ExtendPixPix가를 만듭니다.](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0)
