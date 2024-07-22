---
title: 앵커
description: 이미지 앵커(핫스팟). 반복 가능한 텍스처 또는 데칼 재질의 텍스처 기준점(핫스팟)을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2c5dce-6eb1-4f05-80bd-7336deb08b9e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 2%

---

# 앵커{#anchor}

이미지 앵커(핫스팟). 반복 가능한 텍스처 또는 데칼 재질의 텍스처 기준점(핫스팟)을 지정합니다.

`anchor= *`x`*, *`y`*`

`anchorN= *`xn`*, *`yn`*`

<table id="simpletable_1D8E91D8424A424787C4D20C9B040115"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>, <span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>소스 이미지의 왼쪽 위 모서리로부터의 픽셀 오프셋(int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> xn</span>, <span class="varname"> yn</span> </p></td> 
  <td class="stentry"> <p>소스 이미지의 중심에서 정규화된 오프셋(실수, 실수). </p></td> 
 </tr> 
</table>

반복 가능한 텍스처가 비네팅 개체에 적용되어 텍스처 기준점(`anchor=`)이 개체의 텍스처 원점에 있습니다.

데칼 이미지는 비네팅 오브젝트에 적용되어 데칼 기준점은 오브젝트의 데칼 원점에 있습니다. `pos=` 명령을 사용하여 전사 위치를 추가로 조정할 수 있습니다.

`anchorN=0,0` 이미지 앵커를 소스 이미지의 가운데에 배치합니다. `anchorN=-0.5,-0.5` 또는 `anchor=0,0`은(는) 왼쪽 위 모서리에 있고 `anchorN=0.5,0.5`은(는) 소스 이미지의 오른쪽 아래 모서리에 있습니다.

## 속성 {#section-91f929d35cd745ab9e1eeecf45fcedae}

**재질 특성**. `align=2`이거나 재료가 반복 가능한 질감, 배경 무늬 또는 데칼이 아닌 경우 무시됩니다.

## 기본값 {#section-b06d728c2f664c29bacf810eefcbde69}

`catalog::Anchor`(자료가 카탈로그 항목을 기반으로 하는 경우). 그렇지 않으면 `anchor=0,0`(이미지의 왼쪽 상단 모서리)은 반복 가능한 질감 및 배경 무늬에 해당하고, `anchorN=0,0`(이미지의 중앙)은 데칼에 해당합니다.

## 참조 {#section-b18bf0b035644ca5aedebbc64373718e}

[카탈로그::앵커](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-anchor.md#reference-d9b1d49db1fc440686f64b84453297ab) , [정렬=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7)
