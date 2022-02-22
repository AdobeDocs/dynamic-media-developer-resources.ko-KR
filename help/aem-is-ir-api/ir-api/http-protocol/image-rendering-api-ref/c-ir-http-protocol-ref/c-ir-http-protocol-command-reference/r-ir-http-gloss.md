---
title: 광
description: 재료 표면 광택. 재료 서피스의 상대적 광택을 지정합니다. 조명 맵을 선택하고 광택 효과 및 3D 반사의 렌더링을 제어하는 데 사용됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6df6cd05-9462-4c1e-a7ac-efac3461cf11
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 1%

---

# 광{#gloss}

재료 표면 광택. 재료 서피스의 상대적 광택을 지정합니다. 조명 맵을 선택하고 광택 효과 및 3D 반사의 렌더링을 제어하는 데 사용됩니다.

`gloss= *`val`*`

<table id="simpletable_82166CA080AD401180404462FB2407D7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>기본(참조) 광택 값에는 광택(0...100%) 또는 -1. </p></td> 
 </tr> 
</table>

광택 값이 높을수록 일반적으로 더 강하고 더 선명한 반사가 발생하며, 비네트에서 광택 효과가 활성화된 경우 조명 대비가 증가하여 재료 표면의 분광 밝은 영역을 강화합니다. 각 재료 유형( `type=`)은 최소 및 최대 렌더링 효과를 정의합니다. 일부 재료 유형(예: 벽면 용지)의 경우 `gloss=` 은 렌더링 효과의 모양에 미치는 영향을 최소화하지만 다른 재료 유형(예: 석재 또는 세라믹)의 경우 그 효과가 훨씬 더 두드러집니다.

If `illum=-1` 비네트가 여러 조명 맵을 정의하는 경우 `gloss=` 현재 렌더링 작업에 사용되는 조명 맵을 선택합니다. 렌더러는 지정된 광택에 가장 가까운 광택 값을 갖는 조명 맵을 선택합니다.

`gloss=-1` 비네트의 보기 속성에 정의된 대로 선택한 조명 맵의 참조 광택 값을 선택합니다. 이 값을 사용하면 광택 효과가 활성화되더라도 추가 수정 없이 조명 맵이 작성되는 대로 정확하게 사용할 수 있습니다. If `illum=-1` 그런 다음 비네팅 보기에서 첫 번째 조명 맵의 참조 광택 값을 사용합니다.

## 속성 {#section-92c20c7890fc4aad8d1725d1a1f82da6}

재료 속성입니다. 비네트가 여러 조명 맵을 정의하지 않으면 무시됩니다. 또는, `illum=` 비네트에 3D 반사 데이터가 포함되지 않은 경우 이 지정됩니다. 또는 현재 개체가 3D 반사를 지원하지 않거나 비네트에서 광택 효과를 사용하지 않는 경우

## 기본값 {#section-3722fb5f85c24bc29bdf9c92ce04e678}

`attribute::Gloss` 자료가 카탈로그 항목을 기반으로 하는 경우 기본 조명 맵의 참조 광택 값이나 `illum=`.

## 참조 {#section-29f5b761481a4c52a499a2e16e63c70b}

[속성::광택](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb), [type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35), [rough=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180), [glossmap=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a), [illum=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-illum.md#reference-8efe483a30684022bfe711eb73efbee6)
