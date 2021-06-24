---
description: 이미지 크기 조정. 전체 해상도 이미지를 기준으로 하여 레이어 소스 이미지의 비율을 지정합니다.
solution: Experience Manager
title: scale
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: c2cd37de-f81e-4b08-9a3e-ff05a72c363c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 5%

---

# 축소{#scale}

이미지 크기 조정. 전체 해상도 이미지를 기준으로 하여 레이어 소스 이미지의 비율을 지정합니다.

`scale= *`계수`*`

<table id="simpletable_AC596A87494A4213A7D1C76612E8F2FD"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 계수</span> </p> </td> 
  <td class="stentry"> <p>비율 인수(실제, 0.0보다 큼). </p></td> 
 </tr> 
</table>

`scale=1` 일 때는 배율이 적용되지 않습니다. *`factor`* 1.0보다 작으며 1.0보다 큰 경우 소스 이미지가 확대됩니다.

## 속성 {#section-3c7eb45527394fe79b1ddba6c1fcca09}

소스 이미지/마스크 속성입니다. 현재 레이어뿐만 아니라 `size=`이 지정되어 있으면 무시됩니다. `res=`을(를) 무시합니다. `layer=comp`에 대해 지정된 경우 레이어 0에 적용됩니다. 레이어가 이미지나 마스크와 연결되어 있지 않으면 무시됩니다.

## 기본값 {#section-26e64904362342a5a62c5f6598f330c4}

지정하지 않으면 `res=`이 사용됩니다. `res=` 을 지정하지 않으면 이미지가 스케일링되지 않고 사용됩니다.

## 참조 {#section-61a11f30d37341d58c10df759bfff951}

[res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55) ,  [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
