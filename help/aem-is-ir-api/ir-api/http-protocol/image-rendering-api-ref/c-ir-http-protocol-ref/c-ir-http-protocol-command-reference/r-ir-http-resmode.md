---
description: 리샘플링 모드. 렌더링된 이미지를 wid=, hei= 또는 scl=로 지정된 크기로 조정하는 데 사용할 리샘플링 및/또는 보간 알고리즘을 선택합니다.
seo-description: 리샘플링 모드. 렌더링된 이미지를 wid=, hei= 또는 scl=로 지정된 크기로 조정하는 데 사용할 리샘플링 및/또는 보간 알고리즘을 선택합니다.
seo-title: resMode
solution: Experience Manager
title: resMode
topic: Scene7 Image Serving - Image Rendering API
uuid: 106da74a-d7da-4998-a719-c4c69ae36f6b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 12%

---


# resMode{#resmode}

리샘플링 모드. 렌더링된 이미지를 wid=, hei= 또는 scl=로 지정된 크기로 조정하는 데 사용할 리샘플링 및/또는 보간 알고리즘을 선택합니다.

` `resMode=bilin|bicub|sharp2|bisarp&quot;

<table id="table_AF954C101B30473FAFE9930C7B694305"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> 빌린  </span> </p> </td> 
   <td colname="col2"> <p>표준 쌍선형 보간을 선택합니다. 가장 빠른 재샘플링 방법입니다. 일부 앨리어싱 가공물이 발생할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> 쌍두  </span> </p> </td> 
   <td colname="col2"> <p>쌍입방 보간을 선택합니다. 쌍선형 보간보다 CPU가 많이 사용되지만 눈에 띄는 앨리어싱 가공물이 적은 선명한 이미지를 만들어낼 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> sharp2  </span> </p> </td> 
   <td colname="col2"> <p>수정된 Lanczos Window 기능을 보간 알고리즘으로 선택합니다. 쌍입방 보다 더 높은 CPU 비용으로 약간 더 선명하게 결과를 생성할 수 있습니다. </p> <p> <span class="codeph"> sharp </span> 는  <span class="codeph"> sharp2 </span>로 대체되어 앨리어싱 가공물이 발생할 가능성이 낮습니다(Moiré). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 비카르프  </span> </p> </td> 
   <td colname="col2"> <p><span class="keyword"> Adobe Photoshop </span>에서 "쌍입방 선명하게 하기"라고 하는 이미지 크기를 줄이기 위한 <span class="keyword"> Adobe Photoshop </span> 기본 리샘플러를 선택합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-ea7029f37e094d9cb85646b85fbac0ce}

요청 내 어느 곳에서든 발생할 수 있습니다. 최종 이미지 크기 조절이 적용되지 않는 경우 무시됩니다.

## 기본값 {#section-900872fb93dc41efb3e8ad5b62aadc38}

`attribute::ResMode`

## 참조 {#section-16c557a2250e4f04b3e6cbef18add9ce}

[특성::ResMode](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-resmode.md#reference-fdca7eb6d5104fdeae9d6ac42251db82) ,  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)
