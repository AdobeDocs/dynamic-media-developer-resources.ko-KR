---
description: 이미지 크기 조정. 전체 해상도 이미지를 기준으로 이미지의 배율을 조정합니다.
solution: Experience Manager
title: 크기 조절
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 89701a15-a0b6-460d-b0c1-5e25f3305380
TQID: 'https://experienceleague.adobe.com/MDIhDdn2fZiZgZMlEpdEZOwH0dAot4WGBGw2UcHij1I'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 45
ht-degree: 4%

---

# 크기 조절{#scale}

이미지 크기 조정. 전체 해상도 이미지를 기준으로 이미지의 배율을 조정합니다.

`scale= *`요소`*`

<table id="simpletable_AC0974B79E064BA99C1F76461BDE808A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 요소</span></span> </p> </td> 
  <td class="stentry"> <p>배율 계수(실수, &gt;0). </p></td> 
 </tr> 
</table>

## 기본값 {#section-e9e53959b35844579f0f1d7721b71f8e}

지정하지 않으면 이미지가 비율 조정 없이 사용됩니다.

## 예 {#section-d5526953d6434c58bb2388bd936c13b5}

[!DNL http://server/is/agm/myRootId/myImageId?scale=.5]
