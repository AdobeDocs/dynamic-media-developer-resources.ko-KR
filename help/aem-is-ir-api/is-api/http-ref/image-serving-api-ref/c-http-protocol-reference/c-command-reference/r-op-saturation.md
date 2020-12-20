---
description: 채도를 조정합니다. 레이어 또는 합성 이미지의 각 보이는 픽셀의 채도를 변경합니다.
seo-description: 채도를 조정합니다. 레이어 또는 합성 이미지의 각 보이는 픽셀의 채도를 변경합니다.
seo-title: op_saturation
solution: Experience Manager
title: op_saturation
topic: Scene7 Image Serving - Image Rendering API
uuid: 5e987841-0c3b-4f68-96b1-fad8757f3402
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '107'
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

`op_saturation=-100` 이미지의 채도를 완전히 낮춥니다.

## 속성 {#section-9a3cc9ff060049449554dfa69d92fd53}

레이어 명령. `layer=comp`인 경우 현재 레이어나 합성 이미지에 적용됩니다. 효과 레이어에서 무시됩니다.

## 기본값 {#section-ef0e78f55c8b4d22aee09104dad6410a}

`op_saturation=0`를 선택합니다. CMYK 이미지 또는 레이어는 작업이 적용되기 전에 RGB로 변환됩니다.

## 예 {#section-033b272f1b7e4efeb94e841fd8095357}

색상 사진을 조작하여 &quot;키 높은&quot; 모양을 얻을 수 있습니다.

`http://server/myRootId/myImageId?op_saturation=-60&op_brightness=45&op_contrast=-35`
