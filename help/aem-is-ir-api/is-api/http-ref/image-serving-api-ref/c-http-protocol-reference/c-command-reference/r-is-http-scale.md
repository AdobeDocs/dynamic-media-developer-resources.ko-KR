---
description: 이미지 비율 조정 전체 해상도 이미지를 기준으로 한 배율로 레이어 소스 이미지의 비율을 조정합니다.
seo-description: 이미지 비율 조정 전체 해상도 이미지를 기준으로 한 배율로 레이어 소스 이미지의 비율을 조정합니다.
seo-title: scale
solution: Experience Manager
title: 크기 조절
topic: Scene7 Image Serving - Image Rendering API
uuid: f5540df8-60d9-4efc-99fe-733cdc8268ea
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 5%

---


# scale{#scale}

이미지 비율 조정 전체 해상도 이미지를 기준으로 한 배율로 레이어 소스 이미지의 비율을 조정합니다.

`scale= *`인자`*`

<table id="simpletable_AC596A87494A4213A7D1C76612E8F2FD"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 인자</span> </p> </td> 
  <td class="stentry"> <p>비율 인수(실제, 0.0보다 큼). </p></td> 
 </tr> 
</table>

`scale=1` 시에는 크기 조절이 적용되지 않습니다. *`factor`* 1.0보다 작고 1.0보다 크면 소스 이미지가 확대됩니다.

## 속성 {#section-3c7eb45527394fe79b1ddba6c1fcca09}

소스 이미지/마스크 속성입니다. 현재 레이어에 대해 `size=`이(가) 지정되어 있으면 무시됩니다. `res=`을(를) 무시합니다. `layer=comp`에 대해 지정된 경우 레이어 0에 적용됩니다. 레이어가 이미지나 마스크와 연결되어 있지 않으면 무시됩니다.

## 기본값 {#section-26e64904362342a5a62c5f6598f330c4}

지정하지 않으면 `res=`이 사용됩니다. `res=`을(를) 지정하지 않으면 이미지가 비율 조정 없이 사용됩니다.

## 참조 {#section-61a11f30d37341d58c10df759bfff951}

[res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55) ,  [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
