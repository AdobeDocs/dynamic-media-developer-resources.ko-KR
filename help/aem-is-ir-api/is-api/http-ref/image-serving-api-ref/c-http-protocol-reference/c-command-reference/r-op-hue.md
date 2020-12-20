---
description: 색조 조정 레이어나 합성 이미지의 보이는 각 픽셀의 색조를 지정된 양만큼 이동합니다.
seo-description: 색조 조정 레이어나 합성 이미지의 보이는 각 픽셀의 색조를 지정된 양만큼 이동합니다.
seo-title: op_hue
solution: Experience Manager
title: op_hue
topic: Scene7 Image Serving - Image Rendering API
uuid: 23da539e-0192-4dc4-a19b-41aa94a82730
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 1%

---


# op_hue{#op-hue}

색조 조정 레이어나 합성 이미지의 보이는 각 픽셀의 색조를 지정된 양만큼 이동합니다.

`op_hue= *`adj`*`

<table id="simpletable_7DC7ABA384664BDDAA65B8DEEF7859A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>색조 조정 도(-180...+180int). </p></td> 
 </tr> 
</table>

360도 색조 범위를 기반으로 합니다.

## 속성 {#section-55779644700b4c808a624cdf5a04447e}

레이어 명령. `layer=comp`인 경우 현재 레이어나 합성 이미지에 적용됩니다. 효과 레이어에서 무시됩니다. CMYK 이미지 또는 레이어는 작업이 적용되기 전에 RGB로 변환됩니다.

## 기본값 {#section-7314580251f5456fa1f381ec9e99e0bb}

`op_hue=0`을 클릭하여 색조의 변경 없이
