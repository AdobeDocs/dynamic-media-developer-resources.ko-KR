---
description: 원근 변형 원근 변형을 레이어 소스 이미지에 적용하여 사각형으로 지정된 영역을 채웁니다. 레이어의 다른 영역은 투명하게 유지됩니다.
seo-description: 원근 변형 원근 변형을 레이어 소스 이미지에 적용하여 사각형으로 지정된 영역을 채웁니다. 레이어의 다른 영역은 투명하게 유지됩니다.
seo-title: 원근
solution: Experience Manager
title: 원근
topic: Scene7 Image Serving - Image Rendering API
uuid: b22d7b49-db08-48df-80bc-5b7237aea475
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 원근{#perspective}

원근 변형 원근 변형을 레이어 소스 이미지에 적용하여 사각형으로 지정된 영역을 채웁니다. 레이어의 다른 영역은 투명하게 유지됩니다.

`perspective= *``*[, *`prespQuadres옵션`*]`

`perspectiveN= *``*[, *`prespQuadNres옵션`*]`

<table id="simpletable_4BD38BBF53964F7D97B9E58914C97B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> prespQuad</span> </p></td> 
  <td class="stentry"> <p>원근 4방향 픽셀 좌표(8헤알, 쉼표로 구분). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> prespQuadN</span> </p></td> 
  <td class="stentry"> <p>원근 4각형 정규화된 좌표(8헤알, 쉼표로 구분). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> resOptions</span> </p></td> 
  <td class="stentry"> <p>리샘플링 옵션(아래 참조). </p></td> 
 </tr> 
</table>

*`perspQuad`* 합성(또는 레이어 0) 좌표 공간의 4픽셀 좌표 값으로 구성되며, 이는 합성 이미지의 왼쪽 위 모퉁이에서 발생합니다.

`perspQuadN` 4개의 정규화된 좌표 값으로 구성되어 `0.0,0.0` 있습니다. 이 값은 합성/레이어 0 이미지의 왼쪽 위 모퉁이와 오른쪽 아래 모퉁이에 `1.0,1.0` 해당합니다.

입력 이미지가 변형되어 입력 이미지의 왼쪽 위 모퉁이가 첫 번째 좌표 값, 오른쪽 위 `perspQuad[N]`모퉁이가 두 번째 좌표로, 오른쪽 아래 모퉁이가 세 번째 좌표로, 왼쪽 아래 모퉁이가 네 번째 좌표로 매핑됩니다.

>[!NOTE]
>
>`pos=` 변형된 레이어의 위치를 합성 이미지에서 더 넓히는 데 사용할 수 있습니다.

원근 사각형의 좌표는 합성 이미지 외부에 위치할 수 있습니다.

사각형이 원근 변형에 적합하지 않은 경우(예: 두 개 이상의 정점이 일치하거나 세 개 또는 모든 정점이 동일한 선에 있는 경우 또는 사각형이 자체 교차하거나 오목한 경우) 동작이 정의되지 않습니다.

## 품질 고려 사항 {#section-7cc9056afa614300a9b8844d39739fc3}

기본 구현은 품질과 성능 간에 적절한 타협을 만들어내지만, 선명도를 향상시키거나 앨리어스 결함을 줄이기 위해 소스 이미지의 해상도를 높이는 것이 필요할 수 있습니다.

소스가 이미지일 `scale=` 경우 를 사용하여 이미지의 전체 해상도를 기준으로 다른 해상도를 선택합니다. 지정된 `scale=` 값은 더 높은 PTIF 해상도 수준으로 반올림됩니다. 중첩 요청 소스의 경우, 중첩된 요청으로 생성된 이미지의 크기를 조정하여 원하는 선명도를 얻을 수 있습니다. 텍스트 레이어의 경우, 입력 이미지(렌더링된 텍스트)의 해상도는 에 지정된 해상도를 증가시키는 것과 함께 큰 size= 값을 선택하여 조정됩니다 `textAttr=`.

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
   <td> <p> 가장 가까운 이웃. </p> </td> 
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
   <td> <p> <span class="codeph">R3T<span class="varname"> n</span></span> </p> </td> 
   <td> <p> 조정 가능한 지터가 있는 슈퍼 샘플링(<span class="varname"> n</span> 은 0에서 200 사이의 정수 값이어야 함). </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-818e57df0a1b4449888543bc6af77751}

레이어 명령. 현재 레이어나 레이어 0에 적용되는 경우 `layer=comp`입니다. 효과 레이어에서 무시됩니다.

`res=` 는 같은 레이어에 원근감이 있으면 항상 무시됩니다. `size=` 이미지 레이어에 대해 지정할 때 무시됩니다. `size=` 그리고 `res=` 레이어에서 나중에 사용할 수 있도록 `perspective=` 예약되어 있습니다.

## 기본값 {#section-e35683395d514d4eb6b32924e1bf8f2f}

`None`을 클릭하여 원근 변형을 수행하지 않습니다.

## 참조 {#section-e5b71ac4a0724df6bf678dd354cfa51a}

[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b) , [scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065), [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)
