---
description: 이미지 앵커(핫스팟). 반복 가능한 텍스처 또는 디칼 재질의 텍스처 기준점(핫스팟)을 지정합니다.
seo-description: 이미지 앵커(핫스팟). 반복 가능한 텍스처 또는 디칼 재질의 텍스처 기준점(핫스팟)을 지정합니다.
seo-title: 앵커
solution: Experience Manager
title: 앵커
topic: Scene7 Image Serving - Image Rendering API
uuid: 1e695882-f97a-4208-b595-2851b91bdbfe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 앵커{#anchor}

이미지 앵커(핫스팟). 반복 가능한 텍스처 또는 디칼 재질의 텍스처 기준점(핫스팟)을 지정합니다.

`anchor= *``*, *`xy`*`

`anchorN= *``*, *`xnyn`*`

<table id="simpletable_1D8E91D8424A424787C4D20C9B040115"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>, <span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>소스 이미지의 왼쪽 위 모퉁이에서 픽셀 오프셋(int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> xn</span>, <span class="varname"> yn</span> </p></td> 
  <td class="stentry"> <p>소스 이미지의 중심에서 표준화된 오프셋(실제, 실제). </p></td> 
 </tr> 
</table>

반복 가능한 텍스처가 비네팅 개체에 적용되므로 텍스처 기준점( `anchor=`)이 개체의 텍스처 원점에 위치합니다.

비네팅 오브젝트에 디컬된 이미지가 적용되므로 디컬된 앵커 포인트가 오브젝트의 디털 원점에 위치합니다. decal 위치는 `pos=` 명령을 사용하여 추가로 조정할 수 있습니다.

`anchorN=0,0` 소스 이미지의 중앙에 이미지 앵커를 배치합니다. `anchorN=-0.5,-0.5` 또는 `anchor=0,0` 왼쪽 위 모퉁이에 있고 소스 이미지의 오른쪽 아래에 `anchorN=0.5,0.5` 있습니다.

## 속성 {#section-91f929d35cd745ab9e1eeecf45fcedae}

**재료 속성**. 재질이 반복 `align=2`가능한 텍스처, 배경 무늬 또는 디컬이 아닌 경우 무시됩니다.

## 기본값 {#section-b06d728c2f664c29bacf810eefcbde69}

`catalog::Anchor`, if the material is based on a catalog entry. 그렇지 `anchor=0,0` 않으면(이미지의 왼쪽 위 모서리) 반복 가능한 텍스처 및 배경 무늬, `anchorN=0,0` (이미지의 가운데) 디캘의 경우

## 참조 {#section-b18bf0b035644ca5aedebbc64373718e}

[catalog::Anchor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-anchor.md#reference-d9b1d49db1fc440686f64b84453297ab) , [align=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7)
