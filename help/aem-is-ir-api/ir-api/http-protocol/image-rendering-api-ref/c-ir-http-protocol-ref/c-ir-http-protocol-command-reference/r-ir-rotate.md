---
title: 회전
description: 재료 회전 각도. 재료의 회전 각도를 정의합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 355d9691-c04b-44a6-9563-5bef185cfa7e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 4%

---

# 회전{#rotate}

재료 회전 각도. 재료의 회전 각도를 정의합니다.

` rotate= *`각도`*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 각도 </span> </p> </td> 
  <td class="stentry"> <p>도 단위 회전 각도(실수). </p> </td> 
 </tr> 
</table>

평면 개체 또는 평면 개체에 적용할 경우 반복 가능한 질감 재료(배경 무늬 제외)를 45°의 배수로 회전합니다.

[플로우 라인] 및 [스케치 객체]에 적용할 때 반복 가능한 텍스처 재료를 임의의 각도로 회전합니다.

데칼 재료를 임의의 각도로 회전합니다.

양의 각도는 시계 방향으로 회전합니다. 텍스처 또는 데칼이 기준점을 중심으로 회전합니다( `anchor=`); 기준점은 대상 오브젝트의 원점과 정렬된 상태를 유지합니다.

## 속성 {#section-ad4d07897ca24f63af1a4062f8618e36}

재질 속성입니다. 단색, 벽지, 캐비닛 및 창 처리 재료에서 무시됩니다. *`angle`* Flowline 또는 Sketch 개체에 적용되지 않는 한 반복 가능한 텍스처에는 45의 배수여야 합니다.

## 기본값 {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`를 참조하십시오.

## 참조 {#section-f73c00e9368b478dac1fd15bb4367a12}

[앵커=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
