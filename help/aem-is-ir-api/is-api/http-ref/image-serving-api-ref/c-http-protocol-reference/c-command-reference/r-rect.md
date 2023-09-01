---
title: rect
description: 최종 보기 사각형. 이를 통해 최종 보기 이미지를 여러 스트립 또는 타일로 분해할 수 있으며, 이를 별도로 전달하고 클라이언트가 원활하게 재조립할 수 있으며, 가장자리를 따라 아티팩트가 없습니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1870001b-7904-470f-9582-984d453509ca
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 1%

---

# rect{#rect}

최종 보기 사각형. 이를 통해 최종 보기 이미지를 여러 스트립 또는 타일로 분해할 수 있으며, 이를 별도로 전달하고 클라이언트가 원활하게 재조립할 수 있으며, 가장자리를 따라 아티팩트가 없습니다.

`rect= *`주역`*, *`크기`*[, *`크기 조절`*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 주역</span> </p> </td> 
  <td class="stentry"> <p>그 다음, 보기 이미지의 왼쪽 위 모서리에서 보기 사각형(int, int)의 왼쪽 위 모서리까지의 픽셀 오프셋(픽셀 단위) <span class="varname"> 크기 조절</span> 이 적용됩니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 크기</span> </p></td> 
  <td class="stentry"> <p>ROI 크기(픽셀 단위, int, int). 응답 이미지 크기를 지정합니다. 이미지가 다음으로 채워짐 <span class="codeph"> bgc=</span> 뷰 이미지가 표시하지 않는 영역(또는 다음과 같은 경우 투명한 왼쪽)에서 <span class="codeph"> fmt=*-alpha</span> 이(가) 요청에 있습니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> scale</span> </p></td> 
  <td class="stentry"> <p>척도 요소(실수). 1.0보다 작은 값은 해상도를 감소시키고, 1.0보다 큰 값은 해상도를 증가시킵니다. </p></td> 
 </tr> 
</table>

이 명령을 사용하여 이미지 제공은 HTTP를 통해 구성된 크기 제한을 초과하는 큰 이미지를 전달할 수 있습니다. `attribute::MaxPix`.

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

이 정보를 기반으로 4 개의 600x2000 픽셀 스트립이 필요합니다. 다음 `rect=` 명령은 스트립 크기와 위치를 설명하는 데 사용됩니다.

이 이미지는 자주 변경되므로 `id=` 명령이 포함됩니다. 이렇게 하면 CDN 또는 프록시 서버에서 캐시되었을 수 있는 이전 버전의 이미지에서 한 개 이상의 스트립으로 끝날 가능성을 최소화합니다. 값 `image.version` 속성이 이 용도로 사용됩니다.

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## 속성 {#section-aae223cee13e46d38b74680c048d945b}

속성 보기. 이 설정은 현재 레이어 설정에 관계없이 적용됩니다.

뷰 이미지 외부로 연장되는 ROI의 모든 영역은 패딩된다. `bgc=`.

중요 사항 `rect=` 적용됨 *이후* 최종 배율 및 피팅 `scl=`, `wid=`, `hei=`, `fit=`, `rgn=`, 및 `align=`.

## 기본값 {#section-b296d3bbfb19441f87137a452b70f19a}

수정되지 않은 전체 보기 이미지( `rect=0,0,width,height,1.0`).

## 참조 {#section-74015202c0c545ec82aec614d74b4bbd}

[자르기=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47), [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [정렬=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [맞춤=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f), [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5), [id=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0)
