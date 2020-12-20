---
description: 이미지 앵커(핫스팟). 반복 가능한 텍스처 또는 디캘의 텍스처 기준점(핫스팟)을 지정합니다.
seo-description: 이미지 앵커(핫스팟). 반복 가능한 텍스처 또는 디캘의 텍스처 기준점(핫스팟)을 지정합니다.
seo-title: 앵커
solution: Experience Manager
title: 앵커
topic: Scene7 Image Serving - Image Rendering API
uuid: 1e695882-f97a-4208-b595-2851b91bdbfe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 3%

---


# 앵커{#anchor}

이미지 앵커(핫스팟). 반복 가능한 텍스처 또는 디캘의 텍스처 기준점(핫스팟)을 지정합니다.

`anchor= *``*, *`xy`*`

`anchorN= *``*, *`크닌`*`

<table id="simpletable_1D8E91D8424A424787C4D20C9B040115"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>,  <span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>소스 이미지의 왼쪽 위 모서리에서 픽셀 오프셋(int, int)을 반환합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> xn</span>,  <span class="varname"> yn</span> </p></td> 
  <td class="stentry"> <p>소스 이미지의 중앙으로부터 정규화된 오프셋(실제, 실제)입니다. </p></td> 
 </tr> 
</table>

반복 가능한 텍스처가 비네팅 개체에 적용되므로 텍스처 기준점( `anchor=`)이 개체의 텍스처 원점에 있습니다.

비네팅 오브젝트에 디컬한 이미지가 적용되므로 비네팅 기준점은 오브젝트의 디테일 원점에 위치합니다. decal 위치는 `pos=` 명령을 사용하여 추가로 조정할 수 있습니다.

`anchorN=0,0` 소스 이미지의 중앙에 이미지 앵커를 배치합니다. `anchorN=-0.5,-0.5` 소스 이미지 `anchor=0,0` 의 왼쪽 위 모서리 `anchorN=0.5,0.5` 에 있고 오른쪽 아래 모서리에 있습니다.

## 속성 {#section-91f929d35cd745ab9e1eeecf45fcedae}

**재료 속성**. `align=2`이(가) 반복 가능한 텍스처, 배경 무늬 또는 십자가 아닌 경우 무시됩니다.

## 기본값 {#section-b06d728c2f664c29bacf810eefcbde69}

`catalog::Anchor`, 자재가 카탈로그 항목을 기반으로 하는 경우 그렇지 않은 경우 반복 가능한 텍스처 및 바탕 화면(`anchor=0,0` 이미지의 왼쪽 위 모서리)을 위한 경우 `anchorN=0,0`(이미지의 중심).

## 참조 {#section-b18bf0b035644ca5aedebbc64373718e}

[카탈로그::앵커](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-anchor.md#reference-d9b1d49db1fc440686f64b84453297ab) ,  [정렬=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7)
