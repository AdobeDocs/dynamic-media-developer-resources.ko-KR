---
title: qlt
description: Jpeg 품질입니다. 압축 수준을 제어할 JPEG 인코딩 특성을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 49af2620-081f-4bcc-8245-5aa6bab89a05
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 7%

---

# qlt{#qlt}

Jpeg 품질입니다. 압축 수준을 제어할 JPEG 인코딩 특성을 지정합니다.

` qlt= *`품질`*[. *`채도`*]`

<table id="simpletable_A245B6A3D2374A6A89DE63A5621CFEC0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 품질 </span> </p> </td> 
  <td class="stentry"> <p>JPEG 인코딩 품질(1...100) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 크로마 </span> </p> </td> 
  <td class="stentry"> <p>JPEG 색도 다운샘플링(0=보통, 1=비활성화), 선택 사항, 기본값은 0입니다. </p> </td> 
 </tr> 
</table>

압축 수준을 제어할 JPEG 인코딩 특성을 지정합니다. 결과적으로 파일 크기(응답 데이터의 양)와 결과 이미지의 시각적 품질이 서로 다릅니다.

*`quality`* 값이 높을수록 파일 크기와 품질이 높아지고, 값이 낮을수록 파일 크기가 줄어들고 이미지 품질이 느려집니다. 값이 90보다 큰 경우 압축되지 않은 이미지와 구분할 수 없는 이미지가 생성되는 경우가 많습니다.

일반 JPEG 인코더에서 사용하는 색도 다운샘플링을 비활성화하려면 *`chroma`* 플래그를 설정하십시오. 이 설정은 에지가 밝기가 아닌 색조의 변화에 의해 정의될 때 이미지에서 에지의 인지된 선명도를 증가시킬 수 있다. 이 플래그를 설정하면 파일 크기가 약간 증가할 수 있습니다. 텍스트가 약간 흐리게 보이는 경우 이 설정을 실험해 보십시오.

## 속성 {#section-897b61c786dd4230a2c5807f2f40e722}

요청의 어느 위치에서나 발생할 수 있습니다.

출력 이미지 형식이 JPEG 압축을 지원하지 않는 경우 무시됩니다. JPEG 압축을 지원하는 출력 이미지 형식 목록을 보려면 `fmt=`의 설명을 참조하십시오.

## 기본값 {#section-1c1257df843c475bbac6aadaffcb6347}

`attribute::JpegQuality`

## 참조 {#section-61871fbded3a42f68cf3bdcaed35eae1}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [특성::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50)
