---
description: 이미지를 회전합니다. 이미지, 텍스트 또는 단색 레이어를 지정된 각도로 회전합니다.
solution: Experience Manager
title: 회전
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9f1b2d6f-4e67-4530-9ec6-870b97687ce0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 3%

---

# 회전{#rotate}

이미지를 회전합니다. 이미지, 텍스트 또는 단색 레이어를 지정된 각도로 회전합니다.

`rotate= *`각도`*`

<table id="simpletable_5531ED4C2099411DB404657E12B05314"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 각도</span> </p> </td> 
  <td class="stentry"> <p>회전 각도(실제). </p></td> 
 </tr> 
</table>

양각이 시계 방향으로 회전한다. 레이어 고정점( `anchor=` 또는 `catalog::Anchor`)은 회전 중심으로 사용됩니다. 필요에 따라 레이어 사각형이 확대되어 회전된 데이터 주위에 끼웁니다. 레이어의 배경 영역을 `color=`으로 채운 후 회전이 적용됩니다. `bgColor=` 회전 후 테두리 사각형에 배경색을 추가하는 데 사용할 수 있습니다.

## 속성 {#section-8b5a9bb9062f48dbb8d4e9953ff39e39}

레이어 명령. `layer=comp` 인 경우 현재 레이어 또는 레이어 0에 적용됩니다. 효과 레이어에서 무시됨.

## 기본값 {#section-69475db636124a8a85f132b6d49bd592}

`rotate=0`를 설정하는 것이 좋습니다.

## 예 {#section-e8ab3ba8a8624b43aeaaa8f089fc2f00}

이미지 카탈로그의 이미지 왼쪽 위 모서리 근처에 &quot;판매 중&quot; 레이블을 배치합니다. 레이블 이미지의 크기가 이미 300x300 보기에 대해 올바르게 지정되었으므로 왼쪽으로 30도 회전해야 합니다. 텍스트 상자를 흰색 반불투명 색상으로 칠하여 레이블을 향상시킵니다.

`http:// *`서버`*/myRootId/myImageId?scl=1&size=300,300&origin=-0.5,-0.5 &layer=1&src=labelImage&origin=-0.5,-0.5&rotate=-30&color=ffffff40`

`wid=` 및 `hei=`를 사용하는 대신 레이어 0에 `size=`을 적용하여 보기 크기를 설정합니다. 이렇게 하면 `labelImage`의 최종 크기를 변경하지 않고 `myImageId` 크기를 조정할 수 있습니다. 또한 `scl=1`을 지정해야 합니다. 그렇지 않으면 합성 이미지의 크기가 `attribute::DefaultPix`로 조정될 수 있습니다(0,0 로 설정되지 않은 경우). `color=` 회전 전에 텍스트 상자에 반불투명 배경색을 추가합니다.

두 레이어의 원점은 왼쪽 위 모서리로 설정되므로 원하는 정렬을 할 수 있습니다. 레이어 1의 원점은 회전된 후 `labelImage`에 적용됩니다.

회전된 텍스트의 예는 [템플릿](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)에서 [예제 A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac)를 참조하십시오.

## 참조 {#section-c371ee0845994b7382c02e782d1bc595}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) ,  [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab),  [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
