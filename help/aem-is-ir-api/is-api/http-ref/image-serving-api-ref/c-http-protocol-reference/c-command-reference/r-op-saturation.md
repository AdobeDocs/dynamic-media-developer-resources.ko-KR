---
title: op_saturation
description: 채도를 조정합니다. 레이어 또는 합성 이미지의 각 보이는 픽셀의 채도를 변경합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cd71e27e-6ccc-4ade-9bcf-af8e41bcf381
TQID: 'https://experienceleague.adobe.com/lTgjlQNmfVcS1XswABjicGEHjDUO1PVjM7wD1Zi6o2M'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 93
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
