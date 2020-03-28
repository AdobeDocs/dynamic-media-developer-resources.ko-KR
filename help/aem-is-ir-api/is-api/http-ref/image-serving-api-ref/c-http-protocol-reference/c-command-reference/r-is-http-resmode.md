---
description: 리샘플링 모드. 이미지 데이터 크기 조정에 사용할 리샘플링 및/또는 보간 알고리즘을 선택합니다. 또한 보기 변형 동안 텍스트 레이어의 회전 및 합성 이미지의 크기 조절에 적용됩니다.
seo-description: 리샘플링 모드. 이미지 데이터 크기 조정에 사용할 리샘플링 및/또는 보간 알고리즘을 선택합니다. 또한 보기 변형 동안 텍스트 레이어의 회전 및 합성 이미지의 크기 조절에 적용됩니다.
seo-title: resMode
solution: Experience Manager
title: resMode
topic: Scene7 Image Serving - Image Rendering API
uuid: 8e12aa06-072c-4e7a-84e6-01437c43c57b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# resMode{#resmode}

리샘플링 모드. 이미지 데이터 크기 조정에 사용할 리샘플링 및/또는 보간 알고리즘을 선택합니다. 또한 보기 변형 동안 텍스트 레이어의 회전 및 합성 이미지의 크기 조절에 적용됩니다.

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 빌린 </span> </p> </td> 
   <td colname="col2"> <p>표준 양방향 보간을 선택합니다. 가장 빠른 재샘플링 방법입니다. 일부 앨리어싱 가공물이 발생할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 쌍두 </span> </p> </td> 
   <td colname="col2"> <p>양방향 보간을 선택합니다. 양방향 선형 보간보다 CPU가 많이 사용되지만 눈에 띄는 앨리어스 가공물이 적은 선명한 이미지를 만들어낼 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sharp2 </span> </p> </td> 
   <td colname="col2"> <p>수정된 Lanczos Window 기능을 보간 알고리즘으로 선택합니다. 쌍3차보다 더 선명한 결과를 생성하지만 CPU 사용이 증가할 수 있습니다. <span class="codeph"> sharp </span> 는 <span class="codeph"> </span>sharp2로 대체되었으며, 앨리어스 가공물이 발생할 가능성이 낮습니다(Moiré). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 비바프 </span> </p> </td> 
   <td colname="col2"> <p>Adobe Photoshop에서 "쌍입방 더 선명하게"라고 하는 이미지 크기를 줄이기 위해 Photoshop 기본 리샘플러를 선택합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-a171bacf4ddf43c782e46b86a16d443e}

요청 속성입니다. 모든 레이어 크기 조정을 포함하여 최종 응답 이미지 만들기와 관련된 모든 크기 조정 작업에 적용됩니다.

## 기본값 {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## 예 {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

이미지 카탈로그에 저장된 레이어가 있는 이미지의 고품질 변환을 검색합니다. 이미지에 텍스트가 포함될 수 있습니다. 이미지 편집 응용 프로그램에서 추가 프로세스를 진행할 예정이므로 이미지에 알파 채널을 요청합니다.

` http:// *`서버`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## 참조 {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[속성::ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
