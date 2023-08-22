---
title: scale
description: 이미지 크기 조정. 전체 해상도 이미지를 기준으로 레이어 소스 이미지의 비율을 조정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2cd37de-f81e-4b08-9a3e-ff05a72c363c
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 4%

---

# scale{#scale}

이미지 크기 조정. 전체 해상도 이미지를 기준으로 레이어 소스 이미지의 비율을 조정합니다.

`scale= *`요소`*`

<table id="simpletable_AC596A87494A4213A7D1C76612E8F2FD"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 요소</span> </p> </td> 
  <td class="stentry"> <p>배율 계수(실수, 0.0보다 큼). </p></td> 
 </tr> 
</table>

다음과 같은 경우에는 배율이 적용되지 않습니다. `scale=1`. *`factor`* 축소율이 1.0보다 작고 1.0보다 크면 소스 이미지가 확대됩니다.

## 속성 {#section-3c7eb45527394fe79b1ddba6c1fcca09}

소스 이미지/마스크 속성. 다음과 같은 경우 무시됨 `size=` 는 현재 레이어에도 지정됩니다. 재정의 `res=`. 다음에 대해 지정된 경우 레이어 0에 적용됩니다. `layer=comp`. 레이어가 이미지 또는 마스크와 연결되어 있지 않으면 무시됩니다.

## 기본값 {#section-26e64904362342a5a62c5f6598f330c4}

지정하지 않으면 `res=` 를 사용합니다. If `res=` 을 지정하지 않으면 이미지가 비율 조정 없이 사용됩니다.

## 참조 {#section-61a11f30d37341d58c10df759bfff951}

[res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55) , [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
