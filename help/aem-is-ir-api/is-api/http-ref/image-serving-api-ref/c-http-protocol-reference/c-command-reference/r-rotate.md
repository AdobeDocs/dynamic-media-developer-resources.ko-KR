---
title: 회전
description: 이미지를 회전합니다. 이미지, 텍스트 또는 단색 레이어를 지정된 각도만큼 회전합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9f1b2d6f-4e67-4530-9ec6-870b97687ce0
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 2%

---

# 회전{#rotate}

이미지를 회전합니다. 이미지, 텍스트 또는 단색 레이어를 지정된 각도만큼 회전합니다.

`rotate= *`각도`*`

<table id="simpletable_5531ED4C2099411DB404657E12B05314"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 각도</span> </p> </td> 
  <td class="stentry"> <p>도 단위 회전 각도(실수). </p></td> 
 </tr> 
</table>

양의 각도는 시계 방향으로 회전합니다. 레이어 기준점(`anchor=` 또는 `catalog::Anchor`)이 회전 중심 역할을 합니다. 레이어 사각형은 자르기를 방지하기 위해 필요에 따라 확대되고 회전된 데이터 주위에 맞춰집니다. 레이어의 배경 영역을 `color=`(으)로 채운 후 회전이 적용됩니다. 수정자 `bgColor=`을(를) 사용하여 회전 후 테두리 사각형에 배경색을 추가할 수 있습니다.

## 속성 {#section-8b5a9bb9062f48dbb8d4e9953ff39e39}

레이어 명령. `layer=comp`인 경우 현재 레이어 또는 레이어 0에 적용됩니다. 효과 레이어에서 무시됨.

## 기본값 {#section-69475db636124a8a85f132b6d49bd592}

`rotate=0`(순환 없음).

## 예 {#section-e8ab3ba8a8624b43aeaaa8f089fc2f00}

이미지 카탈로그의 이미지 왼쪽 상단 모서리 근처에 &quot;판매 중&quot; 레이블을 배치합니다. 레이블 이미지의 크기가 이미 300x300 보기에 맞게 조정되었으므로 왼쪽으로 30° 회전해야 합니다. 레이블을 향상시키려면 텍스트 상자를 흰색의 반불투명 색상으로 채웁니다.

`http:// *`서버`*/myRootId/myImageId?scl=1&size=300,300&origin=-0.5,-0.5 &layer=1&src=labelImage&origin=-0.5,-0.5&rotate=-30&color=ffffff40`

`size=` 및 `wid=`을(를) 사용하지 않고 레이어 0에 `hei=`을(를) 적용하여 보기 크기를 설정합니다. 이 메서드를 사용하면 `myImageId`의 최종 크기를 변경하지 않고 `labelImage`의 크기를 조정할 수 있습니다. 또한 `scl=1`을(를) 지정하십시오. 그렇지 않으면 합성 이미지가 `attribute::DefaultPix`(0,0(으)로 설정되지 않은 경우)로 조정될 수 있습니다. 수정자 `color=`은(는) 회전 전에 텍스트 상자에 반불투명 배경색을 추가합니다.

두 레이어의 원점을 왼쪽 위 모서리로 설정하여 원하는 정렬을 수행합니다. 레이어 1의 원점은 회전한 후 `labelImage`에 적용됩니다.

회전된 텍스트의 예제는 [템플릿](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac)의 [예제 A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)을(를) 참조하십시오.

## 참조 {#section-c371ee0845994b7382c02e782d1bc595}

[앵커=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab), [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
