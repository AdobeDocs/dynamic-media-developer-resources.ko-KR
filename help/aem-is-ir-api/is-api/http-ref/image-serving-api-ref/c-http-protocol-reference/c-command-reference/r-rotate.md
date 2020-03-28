---
description: 이미지를 회전합니다. 이미지, 텍스트 또는 단색 레이어를 지정된 각도로 회전합니다.
seo-description: 이미지를 회전합니다. 이미지, 텍스트 또는 단색 레이어를 지정된 각도로 회전합니다.
seo-title: 회전
solution: Experience Manager
title: 회전
topic: Scene7 Image Serving - Image Rendering API
uuid: 160d3c4b-3871-43bd-a17d-96198c7ea839
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# rotate{#rotate}

이미지를 회전합니다. 이미지, 텍스트 또는 단색 레이어를 지정된 각도로 회전합니다.

`rotate= *`각도`*`

<table id="simpletable_5531ED4C2099411DB404657E12B05314"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 각도</span> </p> </td> 
  <td class="stentry"> <p>회전 각도(도 단위)(실제). </p></td> 
 </tr> 
</table>

양수 각도는 시계 방향으로 회전합니다. 레이어 기준점( `anchor=` 또는 `catalog::Anchor`)은 회전 중심 역할을 합니다. 필요에 따라 레이어 사각형이 확대되어 회전된 데이터 주위에 맞춰져 잘리지 않습니다. 레이어의 배경 영역을 다음으로 채운 후에 회전이 적용됩니다 `color=`. `bgColor=` 회전 후 경계 사각형에 배경색을 추가하는 데 사용할 수 있습니다.

## 속성 {#section-8b5a9bb9062f48dbb8d4e9953ff39e39}

레이어 명령. 현재 레이어나 레이어 0에 적용되는 경우 `layer=comp`입니다. 효과 레이어에서 무시됩니다.

## 기본값 {#section-69475db636124a8a85f132b6d49bd592}

`rotate=0`을 클릭합니다.

## 예 {#section-e8ab3ba8a8624b43aeaaa8f089fc2f00}

이미지 카탈로그의 왼쪽 위 모서리 근처에 &quot;판매 중&quot; 레이블을 배치합니다. 레이블 이미지가 이미 300x300 보기에 대해 올바르게 크기가 지정되었으며 왼쪽으로 30도 회전해야 합니다. 텍스트 상자를 흰색 반불투명 색상으로 칠하여 레이블을 향상시킵니다.

`http:// *`서버`*/myRootId/myImageId?scl=1&size=300,300&origin=-0.5,-0.5 &layer=1&src=labelImage&origin=-0.5,-0.5&rotate=-30&color=ffffff40`

Adobe `size=` 는 및 를 사용하는 대신 레이어 0을 적용하여 보기 크기를 `wid=` 설정합니다 `hei=`. 이렇게 `myImageId` 하면 최종 크기를 변경하지 않고 크기를 조정할 수 `labelImage`있습니다. 또한 지정해야 `scl=1`합니다. 그렇지 않으면 합성 이미지의 크기를 0,0 `attribute::DefaultPix` 으로 설정하지 않으면 크기를 조정할 수 있습니다. `color=` 회전 전에 텍스트 상자에 반불투명 배경색을 추가합니다.

두 레이어의 원점은 왼쪽 위 모퉁이로 설정되어 원하는 정렬을 수행합니다. 레이어 1의 원점은 회전한 `labelImage`후에 적용됩니다.

회전된 [텍스트의 예는](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) 템플릿의 [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) A 예를 참조하십시오.

## 참조 {#section-c371ee0845994b7382c02e782d1bc595}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab), [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
