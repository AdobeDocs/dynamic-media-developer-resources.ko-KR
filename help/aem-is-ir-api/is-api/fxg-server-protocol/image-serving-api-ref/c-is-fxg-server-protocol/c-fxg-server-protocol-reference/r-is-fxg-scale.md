---
description: 이미지 크기 조정. 전체 해상도 이미지에 대해 요소를 기준으로 이미지를 배율합니다.
solution: Experience Manager
title: scale
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 89701a15-a0b6-460d-b0c1-5e25f3305380
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 8%

---

# 축소{#scale}

이미지 크기 조정. 전체 해상도 이미지에 대해 요소를 기준으로 이미지를 배율합니다.

`scale= *`계수`*`

<table id="simpletable_AC0974B79E064BA99C1F76461BDE808A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 계수</span></span> </p> </td> 
  <td class="stentry"> <p>비율 인수(실수, 0 이상). </p></td> 
 </tr> 
</table>

## 기본값 {#section-e9e53959b35844579f0f1d7721b71f8e}

지정하지 않으면 이미지가 스케일링 없이 사용됩니다.

## 예 {#section-d5526953d6434c58bb2388bd936c13b5}

[!DNL http://server/is/agm/myRootId/myImageId?scale=.5]
