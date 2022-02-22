---
title: 거칠게
description: 재료 서피스 거칠기. 재료 서피스의 상대적 거칠기를 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8903b51c-c7d4-460f-8f28-00053eac9d6e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---

# 거칠게{#rough}

재료 서피스 거칠기. 재료 서피스의 상대적 거칠기를 지정합니다.

` rough= *`val`*`

<table id="simpletable_432E33EC87144AC7A2A8D9406F862708"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>기본 거칠기를 선택하려면 서피스 거칠기(0...100%) 또는 -1입니다. </p> </td> 
 </tr> 
</table>

3D 반사 렌더링 효과를 제어하는 데 사용됩니다. 거칠기 값이 낮을수록 일반적으로 더 부드러운 반사 효과가 발생합니다. 값이 높을수록 반영된 이미지의 무작위 지정 및 비산이 발생합니다.

각 재료 유형( `type=`)은 거칠기에 따라 최소 및 최대 반사 렌더링 효과를 정의합니다. 일부 재료 유형(예: 벽면 용지)의 경우 `rough=` 는 반사 모양에 영향을 거의 주지 않지만 다른 재료 유형(예: 석재 또는 세라믹)의 경우 그 효과가 훨씬 더 두드러집니다.

`rough=-1` 거칠기를 서버 내부 기본값으로 설정합니다(일반적인 재료 유형의 경우 40%).

## 속성 {#section-515375758b254c80af576271bdb61bb8}

재료 속성입니다. 비네트에 3D 반사 기능이 없거나 대상 개체에 연관된 3D 형상이 없거나 대상 개체가 장면에 다른 개체를 반영하지 않는 경우 무시됩니다.

## 기본값 {#section-11861a5e6e8649ee988267d2707fd7cc}

`catalog::Roughness` 자재가 카탈로그 항목을 기반으로 하는 경우, 그렇지 않으면 약 40% 입니다.

## 참조 {#section-d232fff7237443cc95c4bb50cb3d32bb}

[type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35) , [광택=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
