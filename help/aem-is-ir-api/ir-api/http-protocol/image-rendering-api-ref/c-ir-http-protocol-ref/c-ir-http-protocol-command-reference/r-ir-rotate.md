---
description: 질감 회전 각도. 재질의 회전 각도를 정의합니다.
seo-description: 질감 회전 각도. 재질의 회전 각도를 정의합니다.
seo-title: 회전
solution: Experience Manager
title: 회전
topic: Scene7 Image Serving - Image Rendering API
uuid: 497cd8ea-c6a4-45d2-b5e0-0898ac00913d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 7%

---


# rotate{#rotate}

질감 회전 각도. 재질의 회전 각도를 정의합니다.

` rotate= *`각도`*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 각도 </span> </p> </td> 
  <td class="stentry"> <p>회전 각도(도 단위(실제). </p> </td> 
 </tr> 
</table>

평면 개체 또는 평면 개체에 적용할 때 반복 가능한 텍스처 재료(배경 무늬 제외)를 45도의 배수로 회전합니다.

플로우 및 스케치 개체에 적용할 때 임의의 각도로 반복 가능한 텍스처 재질을 회전할 수 있습니다.

임의의 각도로 디컬한 재질을 회전합니다.

양각도는 시계 방향으로 회전합니다. 텍스처 또는 디캘이 기준점을 중심으로 회전합니다( `anchor=`).기준점은 대상 개체의 원점에 맞춰 정렬됩니다.

## 속성 {#section-ad4d07897ca24f63af1a4062f8618e36}

재료 속성. 단색, 벽지, 캐비닛 및 윈도우 처리 자료에 의해 무시되었습니다. *`angle`* 순서도나 스케치 개체에 적용되지 않는 경우 반복 가능한 텍스처에 대해 45의 배수여야 합니다.

## 기본값 {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`를 선택합니다.

## 참조 {#section-f73c00e9368b478dac1fd15bb4367a12}

[앵커=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
