---
description: 재료 서피스 거칠음. 재료 서피스의 상대 거칠음을 지정합니다.
seo-description: 재료 서피스 거칠음. 재료 서피스의 상대 거칠음을 지정합니다.
seo-title: 거친
solution: Experience Manager
title: 거친
topic: Scene7 Image Serving - Image Rendering API
uuid: d3b4ece1-cc2a-4012-ad81-2f313d3a370b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 2%

---


# 거친{#rough}

재료 서피스 거칠음. 재료 서피스의 상대 거칠음을 지정합니다.

` rough= *`val`*`

<table id="simpletable_432E33EC87144AC7A2A8D9406F862708"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>기본 거칠음을 선택하려면 서피스 거칠음(0...100%) 또는 -1을 선택합니다. </p> </td> 
 </tr> 
</table>

3D 반사 렌더링 효과를 제어하는 데 사용됩니다. 낮은 거칠음 값은 일반적으로 더 매끄러운 반사 효과를 만듭니다.값이 높을수록 반영된 이미지의 임의화 및 분산이 발생합니다.

각 재료 유형( `type=`)은 거칠기에 따라 최소 및 최대 반사 렌더링 효과를 정의합니다. 일부 재료 유형(예: 벽 용지)의 경우 `rough=`은 반사 모양에 거의 영향을 주지 않지만 다른 재료 유형(예: 돌 또는 도자기)의 경우 효과가 상당히 더 두드러집니다.

`rough=-1` 거칠음을 서버 내부 기본값(일반 재료 유형의 경우 40%)으로 설정합니다.

## 속성 {#section-515375758b254c80af576271bdb61bb8}

재료 속성. 비네팅에 3D 반사 기능이 없거나 대상 개체에 3D 도형이 연결되어 있지 않거나 대상 객체가 장면에 있는 다른 객체를 반영하고 있지 않은 경우 무시됩니다.

## 기본값 {#section-11861a5e6e8649ee988267d2707fd7cc}

`catalog::Roughness` 자료가 카탈로그 항목을 기반으로 하는 경우 약 40%입니다.

## 참조 {#section-d232fff7237443cc95c4bb50cb3d32bb}

[type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35) ,  [글로스=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
