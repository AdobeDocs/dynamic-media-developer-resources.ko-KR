---
description: 색조 조정. 레이어 또는 합성 이미지의 각 보이는 픽셀의 색상을 지정된 양만큼 이동합니다.
solution: Experience Manager
title: op_hue
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b436bd31-12a9-42ed-9ad3-5ff91e3ccce9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 2%

---

# op_hue{#op-hue}

색조 조정. 레이어 또는 합성 이미지의 각 보이는 픽셀의 색상을 지정된 양만큼 이동합니다.

`op_hue= *`adj`*`

<table id="simpletable_7DC7ABA384664BDDAA65B8DEEF7859A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>색조 조정(도 - 180...+180int). </p></td> 
 </tr> 
</table>

360도 색조 범위 기반.

## 속성 {#section-55779644700b4c808a624cdf5a04447e}

레이어 명령. `layer=comp` 인 경우 현재 레이어 또는 복합 이미지에 적용됩니다. 효과 레이어에서 무시됨. 작업이 적용되기 전에 CMYK 이미지 또는 레이어가 RGB로 변환됩니다.

## 기본값 {#section-7314580251f5456fa1f381ec9e99e0bb}

`op_hue=0`: 색조를 변경하지 않습니다.
