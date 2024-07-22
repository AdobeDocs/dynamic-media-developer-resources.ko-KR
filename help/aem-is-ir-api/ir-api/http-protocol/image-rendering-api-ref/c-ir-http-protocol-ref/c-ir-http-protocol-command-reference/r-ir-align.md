---
title: 정렬
description: 텍스처 렌더링 정렬. 선택한 비네팅 개체로 정의된 원점 중 사용할 원점을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b76f173-809b-4b41-bf39-6b85f77ab2db
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 3%

---

# 정렬 {#align}

텍스처 렌더링 정렬. 선택한 비네팅 개체로 정의된 원점 중 사용할 원점을 지정합니다.

`align=0|1|2|3|4|5|6`

<table id="simpletable_D15233999E35488EB2F933BD72798E2F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>기본(가운데 일치) 원본. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>지속적인 일치 원본. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>무작위 정렬. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3..6 </p></td> 
  <td class="stentry"> <p>사용자 정의 원본. </p></td> 
 </tr> 
</table>

렌더러는 텍스처 고정점(`anchor=`)이 지정된 원점과 일치하도록 개체에 텍스처를 적용합니다.

각 개체는 최대 6개의 원점(0, 1, 3, 4, 5, 6)을 정의할 수 있습니다. `align` 값이 지정되었지만 해당 원점이 비네팅 개체에 의해 정의되지 않은 경우 기본(가운데 일치) 원점이 사용됩니다.

`align=2` 임의의 텍스처 정렬을 지정합니다. 이 경우 `anchor=`이(가) 효과적으로 무시됩니다.

주로 인접한 물체 사이의 질감의 정렬을 관리하기 위해 실내 장식품용, 아마도 의류 직물에 사용됩니다.

## 속성 {#section-350fadc87dcf4812a8a02d1c3d6697a0}

재질 속성입니다. 벽, 캐비닛, 기기 또는 창 커버 프레임 객체가 선택되어 있거나 재료가 반복 가능한 텍스처가 아닌 경우에는 무시됩니다.

## 기본값 {#section-3231c2854bae4477836b626ac208dd34}

`catalog::Alignment`(자료가 카탈로그 항목을 기반으로 하는 경우), 그렇지 않은 경우 0(가운데 일치).

## 참조 {#section-945d1ce275df487d9d564d4043156c79}

[카탈로그::정렬](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) , [앵커=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
