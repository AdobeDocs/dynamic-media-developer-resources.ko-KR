---
title: 거칠어
description: 재료 표면 거칠기. 재료 서피스의 상대 거칠기를 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8903b51c-c7d4-460f-8f28-00053eac9d6e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 1%

---

# 거칠어{#rough}

재료 표면 거칠기. 재료 서피스의 상대 거칠기를 지정합니다.

` rough= *`val`*`

<table id="simpletable_432E33EC87144AC7A2A8D9406F862708"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 값 </span> </p> </td> 
  <td class="stentry"> <p>기본 거칠기를 선택하는 표면 거칠기(0...100%) 또는 -1 </p> </td> 
 </tr> 
</table>

3D 반사 렌더링 효과를 제어하는 데 사용됩니다. 낮은 거칠기 값은 일반적으로 더 매끄러운 반사 효과를 생성하고, 높은 값은 반사된 이미지의 무작위화 및 산포를 야기한다.

각 재질 유형(`type=`)은 거칠기를 기반으로 최소 및 최대 반사 렌더링 효과를 정의합니다. 일부 재료 유형(예: 벽지)의 경우 `rough=`은(는) 반사 모양에 미치는 영향을 최소화하지만 다른 재료 유형(예: 돌 또는 세라믹)의 경우 효과가 훨씬 더 뚜렷합니다.

`rough=-1` 거칠기를 서버 내부 기본값으로 설정합니다(일반적인 재질 유형의 경우 40%).

## 속성 {#section-515375758b254c80af576271bdb61bb8}

재질 속성입니다. 비네팅에 3D 반사 기능이 없거나 대상 오브젝트에 3D 형상이 연결되어 있지 않거나 대상 오브젝트가 장면의 다른 오브젝트를 반사하지 않는 경우에는 무시됩니다.

## 기본값 {#section-11861a5e6e8649ee988267d2707fd7cc}

`catalog::Roughness` 자료가 카탈로그 항목을 기반으로 하는 경우, 그렇지 않으면 약 40%입니다.

## 참조 {#section-d232fff7237443cc95c4bb50cb3d32bb}

[type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35) , [gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
