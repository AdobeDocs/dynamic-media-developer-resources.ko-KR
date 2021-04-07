---
description: 리샘플링 모드. 이미지 데이터의 크기 조정에 사용할 리샘플링 및/또는 보간 알고리즘을 선택합니다. 또한 텍스트 레이어 회전 및 보기 변형 중에 합성 이미지의 크기 조절에 적용됩니다.
solution: Experience Manager
title: resMode
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
exl-id: 63c1c028-0378-4a38-8018-e358491786d8
translation-type: tm+mt
source-git-commit: b08d1f5b0aa512be4a6e6a4d45d8d4dec15ca1db
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 6%

---

# resMode{#resmode}

리샘플링 모드. 이미지 데이터의 크기 조정에 사용할 리샘플링 및/또는 보간 알고리즘을 선택합니다. 또한 텍스트 레이어 회전 및 보기 변형 중에 합성 이미지의 크기 조절에 적용됩니다.

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 빌린  </span> </p> </td> 
   <td colname="col2"> <p>표준 선형 보간을 선택합니다. 더욱 빨라진 리샘플링 방법;일부 앨리어스 가공물이 눈에 띄습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 쌍두  </span> </p> </td> 
   <td colname="col2"> <p>입방 보간을 선택합니다. 양방향 선형 보간보다 CPU 사용량이 높지만 앨리어싱 가공물이 적은 선명한 이미지를 만들어냅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sharp2  </span> </p> </td> 
   <td colname="col2"> <p>수정된 Lanczos Window 기능을 보간 알고리즘으로 선택합니다. 더 높은 CPU 비용으로 2큐빅보다 약간 더 선명하게 결과를 생성할 수 있습니다. <span class="codeph"> sharp </span> 는  <span class="codeph"> sharp2 </span>로 대체되어 앨리어싱 가공물(Moiré)의 발생 가능성이 낮습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 비카르프  </span> </p> </td> 
   <td colname="col2"> <p>Adobe Photoshop에서 "쌍입방 더 선명하게"라고 하는 이미지 크기를 줄이기 위해 Photoshop 기본 리셀러를 선택합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!IMPORTANT]
>
>`resMode=bisharp` 및 `fit=stretch`을 모두 사용할 때 이미지의 종횡비를 유지하려면 width 매개 변수 또는 height 매개 변수를 사용하는 것이 좋습니다. 두 매개 변수를 모두 정의해야 하는 경우 다음 예제와 같이 다른 레이어에 매개 변수를 줄 바꿈할 수 있습니다.
>
>`/is/image/is/image/companyname?layer=0&src=is(companyname/imagename?wid=30&hei=30&fit=stretch)&resmode=bisharp`

## 속성 {#section-a171bacf4ddf43c782e46b86a16d443e}

요청 속성을 참조하십시오. 모든 레이어 크기 조정을 포함하여 최종 응답 이미지를 만드는 데 관련된 모든 비율 조정 작업에 적용됩니다.

## 기본값 {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## 예 {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

이미지 카탈로그에 저장된 레이어가 있는 이미지의 고품질 변환을 검색합니다. 이미지에 텍스트가 포함될 수 있습니다. 이미지가 이미지 편집 응용 프로그램에서 추가로 처리되므로 이미지가 포함된 알파 채널을 요청합니다.

` http:// *`서버`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## 참조 {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[특성::ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
