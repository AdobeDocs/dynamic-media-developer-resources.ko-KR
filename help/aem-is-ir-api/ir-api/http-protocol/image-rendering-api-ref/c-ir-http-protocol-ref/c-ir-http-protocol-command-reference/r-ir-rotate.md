---
description: 재료 회전 각도. 재료의 회전 각도를 정의합니다.
solution: Experience Manager
title: 회전
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 355d9691-c04b-44a6-9563-5bef185cfa7e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 6%

---

# 회전{#rotate}

재료 회전 각도. 재료의 회전 각도를 정의합니다.

` rotate= *`각도`*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 각도 </span> </p> </td> 
  <td class="stentry"> <p>회전 각도(실제). </p> </td> 
 </tr> 
</table>

평면 객체 또는 평면 객체에 적용할 경우 반복 가능한 텍스쳐 재료(벽지 제외)를 45도의 배수로 회전합니다.

순선과 스케치 개체에 적용할 때 임의의 각도로 반복 가능한 텍스쳐 재료를 회전합니다.

임의의 각도로 디칼 재료를 회전합니다.

양각이 시계 방향으로 회전한다. 텍스처 또는 십자가 기준점( `anchor=`) 주위를 회전합니다.기준점은 대상 개체의 원점과 정렬된 상태로 유지됩니다.

## 속성 {#section-ad4d07897ca24f63af1a4062f8618e36}

재료 속성입니다. 고체 색상, 벽지, 캐비닛, 윈도우 처리 재료에 의해 무시된다. *`angle`* 순서선 또는 스케치 개체에 적용되지 않는 경우 반복 가능한 텍스쳐의 경우 45의 배수여야 합니다.

## 기본값 {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`를 설정하는 것이 좋습니다.

## 참조 {#section-f73c00e9368b478dac1fd15bb4367a12}

[앵커=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
