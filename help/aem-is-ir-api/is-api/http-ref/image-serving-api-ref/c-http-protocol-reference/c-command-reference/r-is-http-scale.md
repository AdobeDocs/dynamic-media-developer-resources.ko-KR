---
description: 이미지 크기 조정 전체 해상도 이미지를 기준으로 레이어 소스 이미지의 크기를 배율합니다.
seo-description: 이미지 크기 조정 전체 해상도 이미지를 기준으로 레이어 소스 이미지의 크기를 배율합니다.
seo-title: scale
solution: Experience Manager
title: scale
topic: Scene7 Image Serving - Image Rendering API
uuid: f5540df8-60d9-4efc-99fe-733cdc8268ea
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# scale{#scale}

이미지 크기 조정 전체 해상도 이미지를 기준으로 레이어 소스 이미지의 크기를 배율합니다.

`scale= *`계수`*`

<table id="simpletable_AC596A87494A4213A7D1C76612E8F2FD"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 계수</span> </p> </td> 
  <td class="stentry"> <p>비율 인수(실제, 0.0보다 큼). </p></td> 
 </tr> 
</table>

No scaling is applied when `scale=1`. *`factor`* 1.0보다 작고 1.0보다 크면 소스 이미지가 확대됩니다.

## 속성 {#section-3c7eb45527394fe79b1ddba6c1fcca09}

소스 이미지/마스크 속성입니다. 현재 레이어에 대해서도 `size=` 지정된 경우 무시됩니다. Overrides `res=`. 에 대해 지정된 경우 레이어 0에 `layer=comp`적용됩니다. 레이어가 이미지나 마스크와 연결되어 있지 않으면 무시됩니다.

## 기본값 {#section-26e64904362342a5a62c5f6598f330c4}

지정하지 않으면 `res=` 사용됩니다. 이 `res=` 값을 지정하지 않으면 이미지가 비율 조정 없이 사용됩니다.

## 참조 {#section-61a11f30d37341d58c10df759bfff951}

[res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55) , [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
