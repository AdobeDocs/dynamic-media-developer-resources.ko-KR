---
title: rect
description: 최종 보기 사각형. 이를 통해 최종 보기 이미지를 여러 스트립 또는 타일로 분해할 수 있으며, 이를 별도로 전달하고 클라이언트가 원활하게 재조립할 수 있으며, 가장자리를 따라 아티팩트가 없습니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1870001b-7904-470f-9582-984d453509ca
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 1%

---

# rect{#rect}

최종 보기 사각형. 이를 통해 최종 보기 이미지를 여러 스트립 또는 타일로 분해할 수 있으며, 이를 별도로 전달하고 클라이언트가 원활하게 재조립할 수 있으며, 가장자리를 따라 아티팩트가 없습니다.

`rect= *`열`*, *`크기`*[, *`크기`*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 열</span> </p> </td> 
  <td class="stentry"> <p><span class="varname"> 눈금</span>이 적용된 후 보기 이미지의 왼쪽 위 모서리에서 보기 사각형(int, int)의 왼쪽 위 모서리까지의 픽셀 오프셋입니다(픽셀 단위). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 크기</span> </p></td> 
  <td class="stentry"> <p>ROI 크기(픽셀 단위, int, int). 응답 이미지 크기를 지정합니다. 이미지가 보기 이미지로 가려지지 않은 영역의 <span class="codeph"> bgc=</span>(또는 요청에 <span class="codeph"> fmt=*-alpha</span>이(가) 있는 경우 투명한 왼쪽)로 채워집니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 배율</span> </p></td> 
  <td class="stentry"> <p>척도 요소(실수). 1.0보다 작은 값은 해상도를 감소시키고, 1.0보다 큰 값은 해상도를 증가시킵니다. </p></td> 
 </tr> 
</table>

이 명령을 사용하면 이미지 제공에서는 HTTP를 통해 `attribute::MaxPix`(으)로 구성된 크기 제한을 초과하는 큰 이미지를 전달할 수 있습니다.

>[!NOTE]
>
>최상의 결과를 얻으려면 JPEG 압축을 사용할 때 스트립 또는 타일 크기가 JPEG 인코딩 타일 크기(16x16 픽셀)의 배수여야 합니다.

## 예 {#section-932fcfcb41d74a29bc929e4430c49601}

인쇄 가능한 CMYK 이미지를 여러 개의 전체 해상도 스트립으로 분리하여 다운로드 파일 크기를 줄입니다. 연속 이미지를 요청한 경우:

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&fmt=tif&icc=WebCoated`

먼저 이미지에 대한 관련 정보를 얻습니다.

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&req=props`

텍스트 응답에는 다음 속성이 포함됩니다.

`image.width=2000 image.height=2400 image.version=37JK6NTvpvC42F5gOuLEVY`

이 정보를 기반으로 4 개의 600x2000 픽셀 스트립이 필요합니다. `rect=` 명령은 스트립 크기와 위치를 설명하는 데 사용됩니다.

이 이미지는 자주 변경되므로 `id=` 명령이 포함됩니다. 이렇게 하면 CDN 또는 프록시 서버에서 캐시되었을 수 있는 이전 버전의 이미지에서 한 개 이상의 스트립으로 끝날 가능성을 최소화합니다. `image.version` 속성 값이 이 용도로 사용됩니다.

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## 속성 {#section-aae223cee13e46d38b74680c048d945b}

속성 보기. 이 설정은 현재 레이어 설정에 관계없이 적용됩니다.

보기 이미지 외부로 확장되는 ROI 영역에 `bgc=`(으)로 패딩됩니다.

중요 `rect=`이(가) `scl=`, `wid=`, `hei=`, `fit=`, `rgn=` 및 `align=`과(와) 함께 최종 크기 조정 및 피팅에 *after*&#x200B;적용됩니다.

## 기본값 {#section-b296d3bbfb19441f87137a452b70f19a}

수정되지 않은 전체 보기 이미지(`rect=0,0,width,height,1.0`)입니다.

## 참조 {#section-74015202c0c545ec82aec614d74b4bbd}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47), [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f), [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5), [id=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0)
