---
description: 원근 변환. 레이어 소스 이미지에 원근 변환을 적용하여 사각형으로 지정된 영역을 채웁니다. 레이어의 다른 영역은 투명하게 유지됩니다.
solution: Experience Manager
title: 원근
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2e0297b0-c9a4-4bbd-9f06-368f722288d4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 2%

---

# 원근{#perspective}

원근 변환. 레이어 소스 이미지에 원근 변환을 적용하여 사각형으로 지정된 영역을 채웁니다. 레이어의 다른 영역은 투명하게 유지됩니다.

`perspective= *``*[, *`perspQuadresOptions`*]`

`perspectiveN= *``*[, *`perspQuadNresOptions`*]`

<table id="simpletable_4BD38BBF53964F7D97B9E58914C97B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuad</span> </p></td> 
  <td class="stentry"> <p>원근 사각형의 픽셀 좌표(8헤알, 쉼표로 구분됨). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuadN</span> </p></td> 
  <td class="stentry"> <p>원근 사각형의 정규화된 좌표(8헤알, 쉼표로 구분됨). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> resOptions</span> </p></td> 
  <td class="stentry"> <p>재샘플링 옵션(아래 참조). </p></td> 
 </tr> 
</table>

*`perspQuad`* 컴포지트 이미지의 왼쪽 위 모서리에서 생성되는 컴포지트(또는 레이어 0) 좌표 공간의 4개 픽셀 좌표 값으로 구성됩니다.

`perspQuadN` 4개의 정규화된 좌표 값으로 구성됩니다. 여기서 `0.0,0.0` 는 컴포지트/레이어 0 이미지의 왼쪽 위 모서리와 오른쪽 아래 모서리 `1.0,1.0` 에 해당합니다.

입력 이미지는 입력 영상의 왼쪽 위 모서리가 제1 좌표 값 `perspQuad[N]`, 제2 좌표의 오른쪽 위 모서리, 제3 좌표의 오른쪽 아래 모서리, 그리고 왼쪽 아래 모서리가 제4 좌표 값에 매핑되도록 변환된다.

>[!NOTE]
>
>`pos=` 합성 이미지에서 형질전환된 레이어를 추가로 배치하는 데 사용할 수 있습니다.

원근 사각형의 좌표는 합성 영상 외측에 위치할 수 있다.

사각형이 원근 변형에 적합하지 않으면 동작이 정의되지 않습니다(예를 들어 두 개 이상의 정점이 일치하거나, 세 개 정점이 동일한 선에 있거나, 사각형이 자체 교차하거나 오목한 경우).

## 품질 고려 사항 {#section-7cc9056afa614300a9b8844d39739fc3}

기본 구현에서는 품질과 성능 간에 합리적인 절충이 가능하지만, 소스 이미지의 해상도를 높여 선명도를 향상시키거나 크기를 줄여 앨리어싱 아티팩트를 줄이는 것이 필요할 수도 있습니다.

소스가 이미지인 경우 `scale=` 을 사용하여 이미지의 전체 해상도를 기준으로 다른 해상도를 선택하십시오. 지정한 `scale=` 값은 다음 더 높은 PTIF 해상도 수준으로 반올림됩니다. 중첩 요청 소스의 경우, 중첩 요청에서 생성한 이미지의 크기를 조정하여 원하는 선명도 얻을 수 있습니다. 텍스트 레이어의 경우 `textAttr=`에 지정된 해상도를 높이는 것과 함께 더 큰 size= 값을 선택하여 입력 이미지(렌더링된 텍스트)의 해상도를 조정합니다.

*`resOptions`* 대체 리샘플링 알고리즘을 선택할 수 있습니다. 다음 값이 지원됩니다(대/소문자 구분).

<table id="table_0F20007986324E228096888ED37219C0"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 값</b> </th> 
   <th class="entry"> <b> 설명</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> R1</span> </p> </td> 
   <td> <p> 가까운 이웃입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R2</span> </p> </td> 
   <td> <p> 쌍1차. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R3</span> </p> </td> 
   <td> <p> 표준 슈퍼 샘플링(기본값). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">R3<span class="varname"> Tn</span></span> </p> </td> 
   <td> <p> 조정 가능한 지터(<span class="varname"> n</span>은 0에서 200 사이의 정수 값이어야 합니다.) </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-818e57df0a1b4449888543bc6af77751}

레이어 명령. `layer=comp` 인 경우 현재 레이어 또는 레이어 0에 적용됩니다. 효과 레이어에서 무시됨.

`res=` 투시가 동일한 레이어에 있으면 항상 무시됩니다. `size=` 이미지 레이어에 대해 지정되면 이 무시됩니다. `size=` 및  `res=` 가 있는 레이어에서는 향후 사용할  `perspective=` 수 있도록 예약되어 있습니다.

## 기본값 {#section-e35683395d514d4eb6b32924e1bf8f2f}

`None`원근 변환 없이 사용할 수 있습니다.

## 참조 {#section-e5b71ac4a0724df6bf678dd354cfa51a}

[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b) ,  [scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065),  [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143),  [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)
