---
title: 원근감
description: 원근감 있는 변환. 레이어 소스 이미지에 원근 변환을 적용하여 사각형으로 지정된 영역을 채웁니다. 레이어의 다른 영역은 투명하게 유지됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2e0297b0-c9a4-4bbd-9f06-368f722288d4
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

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
  <td class="stentry"> <p><span class="varname">개의 resOptions</span> </p></td> 
  <td class="stentry"> <p>재샘플링 옵션(아래 참조) </p></td> 
 </tr> 
</table>

수정자 *`perspQuad`*&#x200B;은(는) 합성 이미지의 왼쪽 상단 모서리에서 시작되는 합성(또는 레이어 0) 좌표 공간의 4개의 픽셀 좌표 값으로 구성됩니다.

수정자 `perspQuadN`은(는) 4개의 정규화된 좌표 값으로 구성됩니다. 여기서 `0.0,0.0`은(는) 합성/레이어 0 이미지의 왼쪽 위 모서리에 해당하고 `1.0,1.0`은(는) 오른쪽 아래 모서리에 해당합니다.

입력 이미지의 왼쪽 위 모서리가 `perspQuad[N]`의 제1 좌표 값에 매핑되고, 오른쪽 위 모서리가 제2 좌표에 매핑되고, 오른쪽 아래 모서리가 제3 좌표에 매핑되고, 왼쪽 아래 모서리가 제4 좌표에 매핑되도록 입력 이미지가 변형된다.

>[!NOTE]
>
>수정자 `pos=`은(는) 변환된 층을 합성 이미지에서 더 위치시키는 데 사용될 수 있다.

상기 원근감 4각좌표는 상기 합성영상의 바깥쪽에 위치할 수 있다.

사각형 변환이 원근 변환에 적합하지 않으면 비헤이비어가 정의되지 않습니다. 예를 들어, 두 개 이상의 정점이 일치하는 경우, 세 개의 정점이나 모든 정점이 동일한 선에 있는 경우 또는 사각형이 자체 교차하거나 오목한 경우 등이 있습니다.

## 품질 고려 사항 {#section-7cc9056afa614300a9b8844d39739fc3}

기본 구현은 품질과 성능 사이에서 적절한 타협을 만들지만 선명도를 향상하기 위해 소스 이미지의 해상도를 높이거나 앨리어싱 아티팩트를 줄이기 위해 소스 이미지의 해상도를 낮춰야 할 수도 있습니다.

원본이 이미지인 경우 `scale=`을(를) 사용하여 이미지의 전체 해상도를 기준으로 다른 해상도를 선택합니다. 지정한 `scale=` 값이 다음으로 높은 PTIF 해상도 수준으로 반올림되었습니다. 중첩된 요청 소스가 있는 경우, 중첩된 요청에 의해 생성된 이미지의 크기는 원하는 선명도를 달성하도록 조정될 수 있다. 텍스트 레이어의 경우 `textAttr=`(으)로 지정된 해상도를 높여 더 큰 size= 값을 선택하여 입력 이미지(렌더링된 텍스트)의 해상도를 조정합니다.

한정자 *`resOptions`*&#x200B;을(를) 사용하면 대체 재샘플링 알고리즘을 선택할 수 있습니다. 다음 값이 지원됩니다(대/소문자 구분).

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
   <td> <p> 조정 가능한 지터(<span class="varname"> n</span>)가 있는 슈퍼 샘플링은 0에서 200 사이의 정수 값이어야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-818e57df0a1b4449888543bc6af77751}

레이어 명령. `layer=comp`인 경우 현재 레이어 또는 레이어 0에 적용됩니다. 효과 레이어에서 무시됨.

동일한 레이어에 원근감이 있는 경우 한정자 `res=`은(는) 항상 무시됩니다. 이미지 레이어에 지정된 한정자 `size=`은(는) 무시됩니다. `perspective=`이(가) 있는 레이어의 수정자 `size=` 및 `res=`은(는) 나중에 사용하도록 예약되었습니다.

## 기본값 {#section-e35683395d514d4eb6b32924e1bf8f2f}

`None`(원근 변환 없음).

## 참조 {#section-e5b71ac4a0724df6bf678dd354cfa51a}

[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b) , [scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065), [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)
