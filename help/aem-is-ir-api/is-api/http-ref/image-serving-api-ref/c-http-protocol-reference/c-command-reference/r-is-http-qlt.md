---
title: qlt
description: JPEG 품질. 압축 수준을 제어할 JPEG 인코딩 특성을 지정합니다. 이렇게 하면 파일 크기(응답 데이터의 양)와 결과 이미지의 시각적 품질이 간접적으로 달라집니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2a611a8-f331-4e01-a262-34340ce67b21
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 6%

---

# qlt{#qlt}

JPEG 품질. 압축 수준을 제어할 JPEG 인코딩 특성을 지정합니다. 이렇게 하면 파일 크기(응답 데이터의 양)와 결과 이미지의 시각적 품질이 간접적으로 달라집니다.

` qlt= *`품질`*[, *`채도`*]`

<table id="simpletable_FB8090D4BEBF42FD83A64A7AAB6D7F92"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 품질 </span> </p> </td> 
  <td class="stentry"> <p>JPEG 인코딩 품질(1...100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 크로마 </span> </p> </td> 
  <td class="stentry"> <p>JPEG 색도 다운샘플링(0=보통, 1=비활성화), 선택 사항, 기본값은 0입니다. </p> </td> 
 </tr> 
</table>

*`quality`* 값이 높을수록 파일 크기와 품질이 높아지고, 값이 낮을수록 파일 크기가 줄어들고 이미지 품질이 느려집니다. 값이 90보다 큰 경우 압축되지 않은 이미지와 구분할 수 없는 이미지가 생성되는 경우가 많습니다.

일반적인 JPEG 인코더에서 사용하는 RGB 색도 다운샘플링을 비활성화하려면 *`chroma`* 플래그를 설정하십시오. 이는 에지가 밝기보다 색조의 변화에 의해 정의될 때 이미지 내의 에지의 지각된 선명도를 증가시킬 수 있다. 이 플래그를 설정하면 파일 크기가 약간 증가할 수 있습니다. 텍스트가 약간 흐리게 보이는 경우 이 설정을 실험해 보십시오.

## 속성 {#section-925a44cbdc9042db8d4eb149cd073d21}

요청 속성입니다. 현재 레이어 설정에 관계없이 적용됩니다. 출력 이미지 파일 형식이 JPEG 인코딩을 지원하지 않는 경우에는 무시됩니다. `fmt=`을(를) 지원하는 출력 이미지 형식에 대한 자세한 내용은 `qlt=`의 설명을 참조하세요.

출력 픽셀 유형이 CMYK 또는 회색인 경우 *`chroma`*&#x200B;이(가) 무시됩니다.

## 기본값 {#section-0d8aa45d84df49e6b846596bbaf7f740}

`attribute::JpegQuality`

## 예 {#section-d7d33871d401433aa51d028823eae7a9}

저대역폭 연결을 통한 전송 속도를 높이기 위한 품질 감소:

`http://server/myRoodId/myImageId?qlt=60&wid=300`

고대역폭 연결을 위한 품질 향상:

`http://server/myRootId/myImageId?qlt=95,1&wid=300`

## 참조 {#section-0074a060bb314ddfa7f4ed23be976507}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [특성::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
