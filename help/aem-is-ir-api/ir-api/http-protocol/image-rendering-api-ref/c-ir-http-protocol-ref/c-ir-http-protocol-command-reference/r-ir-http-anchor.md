---
description: 이미지 앵커(핫스팟). 반복 가능한 텍스쳐 또는 디칼 재질의 텍스쳐 기준점(핫스팟)을 지정합니다.
solution: Experience Manager
title: 앵커
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: ea2c5dce-6eb1-4f05-80bd-7336deb08b9e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 2%

---

# 앵커{#anchor}

이미지 앵커(핫스팟). 반복 가능한 텍스쳐 또는 디칼 재질의 텍스쳐 기준점(핫스팟)을 지정합니다.

`anchor= *``*, *`xy`*`

`anchorN= *``*, *`xnyn`*`

<table id="simpletable_1D8E91D8424A424787C4D20C9B040115"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>,  <span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>소스 이미지의 왼쪽 위 모서리에서 픽셀 오프셋(int, int)입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> xn</span>,  <span class="varname"> yn</span> </p></td> 
  <td class="stentry"> <p>소스 이미지의 중심에서 표준화된 오프셋(실제, 실제)입니다. </p></td> 
 </tr> 
</table>

반복 가능한 텍스처가 비네팅 개체에 적용되어 텍스처 기준점( `anchor=`)이 개체의 텍스처 원점에 위치하도록 합니다.

비네팅 오브젝트에 비네팅 이미지가 적용되어 비네팅 앵커 점이 오브젝트의 끝 원점에 위치한다. 상기 디칼 위치는 상기 `pos=` 명령을 사용하여 더 조정할 수 있다.

`anchorN=0,0` 이미지 앵커를 소스 이미지의 중앙에 배치합니다. `anchorN=-0.5,-0.5` 또는 `anchor=0,0` 는 왼쪽 위 모서리에 있으며 소스 이미지 `anchorN=0.5,0.5` 의 오른쪽 아래 모서리에 있습니다.

## 속성 {#section-91f929d35cd745ab9e1eeecf45fcedae}

**재료 속성**. `align=2` 또는 재질이 반복 가능한 텍스처, 배경 무늬 또는 십자가 아닌 경우 무시됩니다.

## 기본값 {#section-b06d728c2f664c29bacf810eefcbde69}

`catalog::Anchor`: 자재가 카탈로그 항목을 기반으로 하는 경우 그렇지 않으면 반복 가능한 텍스처 및 벽지를 위한 `anchor=0,0`(이미지의 왼쪽 위 모서리)과 해수를 위한 `anchorN=0,0`(이미지의 중심)이 표시됩니다.

## 참조 {#section-b18bf0b035644ca5aedebbc64373718e}

[카탈로그::앵커](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-anchor.md#reference-d9b1d49db1fc440686f64b84453297ab) ,  [정렬=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7)
