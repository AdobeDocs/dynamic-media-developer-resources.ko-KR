---
description: '이미지 마스크 사용. 이미지의 마스크나 알파 채널을 이미지에서 작업을 하는 데 사용하는 방법을 지정합니다(예: colorize=). 효과 레이어에 지정하면 효과를 모 레이어의 배경 영역이나 전체 모 레이어 사각형에 적용할 수 있습니다.'
solution: Experience Manager
title: 마스크 사용
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e99101a1-1747-454c-b0c0-3af3335c0497
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 2%

---

# 마스크 사용{#maskuse}

이미지 마스크 사용. 이미지의 마스크나 알파 채널을 이미지에서 작업을 하는 데 사용하는 방법을 지정합니다(예: colorize=). 효과 레이어에 지정하면 효과를 모 레이어의 배경 영역이나 전체 모 레이어 사각형에 적용할 수 있습니다.

`maskUse=norm|invert|off`

다음 표는 의 효과를 보여줍니다. `maskUse=` 사용 가능 여부 및 레이어 이미지와 연관된 마스크(알파 채널)의 유형에 따라 달라집니다.

<table id="table_B765F6A765F548948531AF26DA0B4360"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 값</b> </th> 
   <th class="entry"> <b> 마스크 없음</b> </th> 
   <th class="entry"> <b> 연결되지 않은 알파(또는 별도의 마스크 이미지)</b> </th> 
   <th class="entry"> <b> 관련(사전 곱함) 알파</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 꺼짐 </span> </p> </td> 
   <td> <p> 불투명 이미지 사각형 </p> </td> 
   <td> <p> 불투명 이미지 사각형 </p> </td> 
   <td> <p> 단색 검정으로 채워진 사각형 위의 이미지 전경 영역 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 규범 </span> </p> </td> 
   <td> <p> 불투명 이미지 사각형 </p> </td> 
   <td> <p> 이미지의 전경 영역 </p> </td> 
   <td> <p> 이미지 또는 레이어의 전경 영역 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 반전 </span> </p> </td> 
   <td> <p> 숨겨진 레이어 </p> </td> 
   <td> <p> 이미지의 배경 영역 </p> </td> 
   <td> <p> 단색 검정으로 채워진 이미지 또는 레이어의 배경 영역 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f36ad1af348e45aeb3eb336544df30b0}

이미지 또는 레이어 속성. 다음과 같은 경우 레이어 0에 적용됩니다. `layer=comp`. 효과 레이어에 지정된 경우 명령은 부모 레이어에서 상속된 마스크를 수정합니다.

의 비헤이비어 `maskUse=` 이미지 마스크를 적용할 수 없는 경우 텍스트 또는 단색 레이어로 지정할 때 가 정의되지 않고 지원되지 않습니다( 로 지정됨). `mask=` 또는 `catalog::Mask`).

## 기본값 {#section-982dd8174641437786dcb3729ace6428}

`maskUse=norm`

## 예 {#section-daa371e9be5547368ff6772342acba0a}

이미지의 배경 영역을 색상화합니다. 이미지 전경은 별도의 마스크 이미지로 정의됩니다. 수정되지 않은 이미지인 경우 맨 위에 색상화된 이미지 배경을 레이어링하여 이 작업을 수행합니다.

`http://server/myRootId/myImageId?layer=1&src=myImageId&mask=myImgMask&maskUse=invert&colorize=0x306090`

## 참조 {#section-f239d8f4ce70434f8d30e482ed60ee5e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) , [마스크=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)
