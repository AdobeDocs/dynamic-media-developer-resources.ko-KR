---
description: Jpeg 품질. 압축 수준을 제어할 JPEG 인코딩 속성을 지정합니다. 이렇게 하면 파일 크기(응답 데이터의 양)와 결과 이미지의 시각적 품질이 간접적으로 달라집니다.
seo-description: Jpeg 품질. 압축 수준을 제어할 JPEG 인코딩 속성을 지정합니다. 이렇게 하면 파일 크기(응답 데이터의 양)와 결과 이미지의 시각적 품질이 간접적으로 달라집니다.
seo-title: qlt
solution: Experience Manager
title: qlt
topic: Scene7 Image Serving - Image Rendering API
uuid: 936607c1-20c3-4f76-b970-614b21c47dea
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# qlt{#qlt}

Jpeg 품질. 압축 수준을 제어할 JPEG 인코딩 속성을 지정합니다. 이렇게 하면 파일 크기(응답 데이터의 양)와 결과 이미지의 시각적 품질이 간접적으로 달라집니다.

` qlt= *``*[, *`qualitychroma`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 품질 </span></span> </p> </td> 
  <td class="stentry"> <p>JPEG 인코딩 품질(1...100int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 크로마 </span></span> </p> </td> 
  <td class="stentry"> <p>JPEG 색채화 다운샘플링(0=normal, 1=disable);선택 사항, 기본값은 0입니다. </p> </td> 
 </tr> 
</table>

Used only if `fmt=jpg`. 그렇지 않으면 무시됨

품질 값이 크면 파일 크기가 증가하고 품질이 향상되며, 값이 작으면 파일 크기가 감소하고 인식되는 이미지 품질이 저하됩니다. 값이 90보다 큰 경우 압축되지 않은 이미지와 구분할 수 없는 이미지가 생성되는 경우가 많습니다.

일반적인 JPEG 인코더에서 사용되는 RGB 색도 다운샘플링을 비활성화하려면 `chroma` 플래그를 설정합니다. 이렇게 하면 가장자리가 명도가 아닌 색조의 변경으로 정의될 때 이미지의 가장자리의 선명도가 높아집니다. 이 플래그를 설정하면 파일 크기가 약간 증가할 수 있습니다. 텍스트가 약간 흐린 경우 이 설정을 사용해 보십시오.

`chroma` 출력 픽셀 유형이 CMYK 또는 회색이면 무시됩니다.

## 예 {#section-a6c263f15c29424a86ef267c96a6630a}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80]
