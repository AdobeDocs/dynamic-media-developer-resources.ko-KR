---
title: 원근감
description: 원근감 있는 변환. 레이어 소스 이미지에 원근 변환을 적용하여 사각형으로 지정된 영역을 채웁니다. 레이어의 다른 영역은 투명하게 유지됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2e0297b0-c9a4-4bbd-9f06-368f722288d4
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 1%

---

# 원근감{#perspective}

원근감 있는 변환. 레이어 소스 이미지에 원근 변환을 적용하여 사각형으로 지정된 영역을 채웁니다. 레이어의 다른 영역은 투명하게 유지됩니다.

`perspective= *`perspQuad`*[, *`resOptions`*]`

`perspectiveN= *`perspQuadN`*[, *`resOptions`*]`

<table id="simpletable_4BD38BBF53964F7D97B9E58914C97B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuad</span> </p></td> 
  <td class="stentry"> <p>원근 4차원 픽셀 좌표(8레알, 쉼표로 구분). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuadN</span> </p></td> 
  <td class="stentry"> <p>원근감 2차원 정규화 좌표(8레알, 쉼표로 구분). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> resOptions</span> </p></td> 
  <td class="stentry"> <p>재샘플링 옵션(아래 참조) </p></td> 
 </tr> 
</table>

*`perspQuad`* 합성 이미지의 왼쪽 위 모서리에 있는 합성(또는 레이어 0) 좌표 공간의 4개의 픽셀 좌표 값으로 구성됩니다.

`perspQuadN` 는 4개의 표준화된 좌표 값으로 구성되며, 여기서 `0.0,0.0` 는 합성/레이어 0 이미지의 왼쪽 위 모서리에 해당하고 `1.0,1.0` 오른쪽 하단에 있습니다.

입력 이미지의 좌측 상단 모서리가 의 제1 좌표값에 매핑되도록 입력 이미지가 변형된다 `perspQuad[N]`를 설정하는 경우 오른쪽 위 모서리는 두 번째 좌표에 연결되고, 오른쪽 아래 모서리는 세 번째 좌표에 연결되고, 왼쪽 아래 모서리는 네 번째 좌표에 연결됩니다.

>[!NOTE]
>
>`pos=` 변환된 층을 복합 이미지 내에 추가로 위치시키기 위해 사용될 수 있다.

상기 원근감 4각좌표는 상기 합성영상의 바깥쪽에 위치할 수 있다.

사각형이 원근 변형에 적합하지 않은 경우(예: 두 개 이상의 정점이 일치하는 경우, 세 개 또는 모든 정점이 동일한 선에 있는 경우, 또는 사각형이 자체 교차하거나 오목한 경우)에는 비헤이비어가 정의되지 않습니다.

## 품질 고려 사항 {#section-7cc9056afa614300a9b8844d39739fc3}

기본 구현은 품질과 성능 사이에서 적절한 타협을 이루지만, 때때로 선명도를 향상시키기 위해 소스 이미지의 해상도를 높이거나 앨리어싱 아티팩트를 줄이기 위해 소스 이미지의 해상도를 낮춰야 할 수도 있습니다.

소스가 이미지인 경우 `scale=` 이미지의 전체 해상도를 기준으로 다른 해상도를 선택합니다. 지정됨 `scale=` 값은 다음으로 높은 PTIF 해상도 수준으로 반올림됩니다. 중첩 요청 소스의 경우, 중첩 요청에 의해 생성된 이미지의 크기는 원하는 선명도를 달성하도록 조정될 수 있다. 텍스트 레이어의 경우 지정된 해상도 증가와 함께 더 큰 size= 값을 선택하여 입력 이미지(렌더링된 텍스트)의 해상도를 조정합니다 `textAttr=`.

*`resOptions`* 대체 재샘플링 알고리즘을 선택할 수 있습니다. 다음 값이 지원됩니다(대/소문자 구분).

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
   <td> <p> 가장 가까운 이웃입니다 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R2</span> </p> </td> 
   <td> <p> 이중선형. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R3</span> </p> </td> 
   <td> <p> 표준 수퍼 샘플링(기본값). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">R3T<span class="varname"> n</span></span> </p> </td> 
   <td> <p> 조정 가능한 지터를 사용한 슈퍼 샘플링 (<span class="varname"> n</span> 은(는) 0에서 200 사이의 정수 값이어야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-818e57df0a1b4449888543bc6af77751}

레이어 명령. 다음과 같은 경우 현재 레이어 또는 레이어 0에 적용됩니다. `layer=comp`. 효과 레이어에서 무시됨.

`res=` 원근이 동일한 레이어에 있는 경우 는 항상 무시됩니다. `size=` 이미지 레이어에 대해 지정되면 이 무시됩니다. `size=` 및 `res=` 다음 포함 레이어 내 `perspective=` 나중에 사용하도록 예약되어 있습니다.

## 기본값 {#section-e35683395d514d4eb6b32924e1bf8f2f}

`None`, 원근 변형 없음

## 참조 {#section-e5b71ac4a0724df6bf678dd354cfa51a}

[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b) , [scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065), [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)
