---
title: op_saturation
description: 채도를 조정합니다. 레이어 또는 합성 이미지의 각 보이는 픽셀의 채도를 변경합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cd71e27e-6ccc-4ade-9bcf-af8e41bcf381
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 2%

---

# op_saturation{#op-saturation}

채도를 조정합니다. 레이어 또는 합성 이미지의 각 보이는 픽셀의 채도를 변경합니다.

`op_saturation= *`adj`*`

<table id="simpletable_5F118A28FE674B06A16F6F19C56B4594"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>채도 조정(-100...+100 int). </p></td> 
 </tr> 
</table>

`op_saturation=-100`은(는) 이미지의 채도를 완전히 줄입니다.

## 속성 {#section-9a3cc9ff060049449554dfa69d92fd53}

레이어 명령. `layer=comp`인 경우 현재 레이어 또는 합성 이미지에 적용됩니다. 효과 레이어에서 무시됨.

## 기본값 {#section-ef0e78f55c8b4d22aee09104dad6410a}

`op_saturation=0`(채도가 변경되지 않음). CMYK 이미지 또는 레이어는 작업을 적용하기 전에 RGB으로 변환됩니다.

## 예 {#section-033b272f1b7e4efeb94e841fd8095357}

색상 사진을 조작하여 &quot;높은 키&quot; 모양을 얻을 수 있습니다.

`http://server/myRootId/myImageId?op_saturation=-60&op_brightness=45&op_contrast=-35`
