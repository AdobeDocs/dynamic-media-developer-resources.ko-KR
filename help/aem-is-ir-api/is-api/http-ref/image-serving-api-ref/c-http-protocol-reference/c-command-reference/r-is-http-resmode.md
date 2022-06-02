---
title: resMode
description: 재샘플링 모드. 이미지 데이터 크기 조절에 사용할 리샘플링 및/또는 보간 알고리즘을 선택합니다. 또한 [보기 변환] 중에 텍스트 레이어의 회전 및 합성 이미지의 크기 조절에 적용됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 63c1c028-0378-4a38-8018-e358491786d8
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 6%

---

# resMode{#resmode}

재샘플링 모드. 이미지 데이터 크기 조절에 사용할 리샘플링 및/또는 보간 알고리즘을 선택합니다. 또한 [보기 변환] 중에 텍스트 레이어의 회전 및 합성 이미지의 크기 조절에 적용됩니다.

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 빌린 </span> </p> </td> 
   <td colname="col2"> <p>표준 양방향 보간을 선택합니다. 가장 빠른 재샘플링 방법 일부 앨리어싱 가공물들은 눈에 띄습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 쌍창 </span> </p> </td> 
   <td colname="col2"> <p>양방향 보간을 선택합니다. 양방향 선형 보간보다 CPU가 많이 사용되지만 눈에 띄는 앨리어싱 가공물이 적은 선명한 이미지를 생성합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sharp2 </span> </p> </td> 
   <td colname="col2"> <p>수정된 Lanczos Window 기능을 보간 알고리즘으로 선택합니다. 더 높은 CPU 비용으로 2입방보다 약간 더 선명한 결과를 생성할 수 있습니다. <span class="codeph"> 날카로운 </span> 이(가) <span class="codeph"> sharp2 </span>- 앨리어싱 아티팩트를 발생할 가능성이 낮습니다(모아레). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 비스트로프 </span> </p> </td> 
   <td colname="col2"> <p>Adobe Photoshop에서 "쌍입방 더 선명하게"라고 하는 이미지 크기를 줄이기 위해 Photoshop 기본 리샘플러를 선택합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!IMPORTANT]
>
>둘 다 사용할 때 이미지의 종횡비를 유지하려면 `resMode=bisharp` 및 `fit=stretch`를 설정하는 것이 좋습니다. 두 매개 변수를 모두 정의해야 하는 경우 다음 예제와 같이 다른 레이어에 래핑할 수 있습니다.
>
>`/is/image/is/image/companyname?layer=0&src=is(companyname/imagename?wid=30&hei=30&fit=stretch)&resmode=bisharp`

## 속성 {#section-a171bacf4ddf43c782e46b86a16d443e}

요청 속성입니다. 모든 레이어 스케일링을 포함하여 최종 회신 이미지 만들기에 관련된 모든 스케일링 작업에 적용됩니다.

## 기본값 {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## 예 {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

이미지 카탈로그에 저장된 계층화된 이미지의 최상의 표현물을 검색합니다. 이미지에 텍스트가 포함될 수 있습니다. 상기 영상은 영상 편집 응용 프로그램에서 추가로 처리되어, 상기 영상으로 알파 채널을 요청한다.

` http:// *`서버`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## 참조 {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[특성::ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
