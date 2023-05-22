---
description: 색조를 조정합니다. 지정된 양만큼 레이어 또는 합성 이미지의 각 보이는 픽셀의 색조를 이동합니다.
solution: Experience Manager
title: op_hue
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b436bd31-12a9-42ed-9ad3-5ff91e3ccce9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 1%

---

# op_hue{#op-hue}

색조를 조정합니다. 지정된 양만큼 레이어 또는 합성 이미지의 각 보이는 픽셀의 색조를 이동합니다.

`op_hue= *`adj`*`

<table id="simpletable_7DC7ABA384664BDDAA65B8DEEF7859A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>색조 조정 단위(-180..+180 int). </p></td> 
 </tr> 
</table>

360도 색조 범위를 기반으로 합니다.

## 속성 {#section-55779644700b4c808a624cdf5a04447e}

레이어 명령. 다음과 같은 경우 현재 레이어 또는 합성 이미지에 적용됩니다. `layer=comp`. 효과 레이어에서 무시됨. CMYK 이미지 또는 레이어는 작업을 적용하기 전에 RGB으로 변환됩니다.

## 기본값 {#section-7314580251f5456fa1f381ec9e99e0bb}

`op_hue=0`, 색조 변경 없음
