---
title: resMode
description: 재샘플링 모드. 이미지 데이터 크기를 조정할 때 사용할 재샘플링 및/또는 보간 알고리즘을 선택합니다. 뷰 변환 중 텍스트 레이어의 회전 및 합성 이미지의 크기 조정에도 적용됩니다.
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

재샘플링 모드. 이미지 데이터 크기를 조정할 때 사용할 재샘플링 및/또는 보간 알고리즘을 선택합니다. 뷰 변환 중 텍스트 레이어의 회전 및 합성 이미지의 크기 조정에도 적용됩니다.

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 빌린 </span> </p> </td> 
   <td colname="col2"> <p>표준 이중선형 보간을 선택합니다. 가장 빠른 리샘플링 방법으로 일부 앨리어싱 아티팩트가 눈에 띕니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bicub </span> </p> </td> 
   <td colname="col2"> <p>쌍입방 보간을 선택합니다. 2선형 보간보다 CPU를 많이 사용하지만 덜 눈에 띄는 앨리어싱 아티팩트가 있는 더 선명한 이미지를 만듭니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sharp2 </span> </p> </td> 
   <td colname="col2"> <p>수정된 Lanczos Window 기능을 보간 알고리즘으로 선택합니다. 높은 CPU 비용으로 2차 큐빅보다 약간 더 선명한 결과를 얻을 수 있습니다. <span class="codeph"> 예리하 </span> 이(가) (으)로 대체되었습니다. <span class="codeph"> sharp2 </span>앨리어싱 아티팩트(Moié)를 유발할 가능성이 더 낮습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bisharp </span> </p> </td> 
   <td colname="col2"> <p>Adobe Photoshop에서 "bicubic sharper"라고 하는 이미지 크기를 줄이기 위해 Photoshop 기본 리샘플러를 선택합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!IMPORTANT]
>
>두 옵션을 모두 사용할 때 이미지의 종횡비를 유지하려면 `resMode=bisharp` 및 `fit=stretch`, width 매개 변수 또는 height 매개 변수를 사용하는 것이 좋습니다. 두 매개변수를 정의해야 하는 경우 다음 예제와 같이 다른 레이어로 래핑할 수 있습니다.
>
>`/is/image/is/image/companyname?layer=0&src=is(companyname/imagename?wid=30&hei=30&fit=stretch)&resmode=bisharp`

## 속성 {#section-a171bacf4ddf43c782e46b86a16d443e}

요청 속성입니다. 모든 레이어 크기 조절을 포함하여 최종 응답 이미지 만들기와 관련된 모든 크기 조절 작업에 적용됩니다.

## 기본값 {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## 예 {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

이미지 카탈로그에 저장된 계층화된 이미지의 최상의 품질 렌디션을 검색합니다. 이미지에는 텍스트가 포함될 수 있습니다. 이미지는 이미지 편집 애플리케이션에서 더 처리되므로, 이미지에 대한 알파 채널을 요청한다.

` http:// *`서버`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## 참조 {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[attribute::ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
