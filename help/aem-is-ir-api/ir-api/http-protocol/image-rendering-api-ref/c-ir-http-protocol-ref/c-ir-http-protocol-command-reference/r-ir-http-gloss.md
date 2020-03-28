---
description: 질감 표면의 매끄러운 광택 재료 서피스의 상대적 광택을 지정합니다. 조명 맵을 선택하고 광택 효과 및 3D 반사의 렌더링을 제어하는 데 사용됩니다.
seo-description: 질감 표면의 매끄러운 광택 재료 서피스의 상대적 광택을 지정합니다. 조명 맵을 선택하고 광택 효과 및 3D 반사의 렌더링을 제어하는 데 사용됩니다.
seo-title: 광택
solution: Experience Manager
title: 광택
topic: Scene7 Image Serving - Image Rendering API
uuid: 3774e08b-d24e-4cf2-8719-32a21bb9bcb6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 광택{#gloss}

질감 표면의 매끄러운 광택 재료 서피스의 상대적 광택을 지정합니다. 조명 맵을 선택하고 광택 효과 및 3D 반사의 렌더링을 제어하는 데 사용됩니다.

`gloss= *`val`*`

<table id="simpletable_82166CA080AD401180404462FB2407D7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 값</span></span> </p></td> 
  <td class="stentry"> <p>광택(0...100%) 또는 -1(기본(참조) 광택 값) </p></td> 
 </tr> 
</table>

광택 값이 높으면 일반적으로 더 강한 반사가 발생하고, 비네팅에서 광택 효과가 활성화되면 조명 대비를 높임으로써 재료 표면의 반사 밝은 영역이 대부분 더 잘립니다. 각 재료 유형( `type=`)은 최소 및 최대 렌더링 효과를 정의합니다. 일부 재료 유형(예: 벽지) `gloss=` , 렌더링 효과 모양에 거의 영향을 주지 않지만 다른 재료 유형(예: 석재 또는 세라믹)의 경우 효과가 상당히 더 두드러집니다.

비네팅이 여러 조명 맵을 정의하는 `illum=-1` 경우 `gloss=` 현재 렌더링 작업에 사용되는 조명 맵을 선택합니다. 렌더러는 지정된 광택에 가장 가까운 광택 값을 갖는 조명 맵을 선택합니다.

`gloss=-1` 비네팅의 보기 속성에 정의된 대로 선택한 조명 맵의 참조 광택 값을 선택합니다. 이렇게 하면 광택 효과가 활성화된 경우에도 추가로 수정 없이 조명 맵이 작성됨과 정확히 동일하게 사용됩니다. 또한 `illum=-1` 비네팅 보기에서 첫 번째 조명 맵의 참조 광택 값이 사용됩니다.

## 속성 {#section-92c20c7890fc4aad8d1725d1a1f82da6}

재료 속성. 비네팅이 여러 조명 맵을 정의하지 않거나 `illum=` 지정된 경우, 비네팅에 3D 반사 데이터가 포함되어 있지 않거나 현재 개체가 3D 반사를 지원하지 않거나 비네팅에서 광택 효과를 사용하지 않는 경우, 무시됨

## 기본값 {#section-3722fb5f85c24bc29bdf9c92ce04e678}

`attribute::Gloss` 자료가 카탈로그 항목을 기반으로 하는 경우 기본 조명 맵이나 지정된 조명 맵의 참조 광택 값을 사용하지 `illum=`않습니다.

## 참조 {#section-29f5b761481a4c52a499a2e16e63c70b}

[attribute::](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb): [type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35), [rough=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180), [glossmap=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a)[, glossum=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-illum.md#reference-8efe483a30684022bfe711eb73efbee6)
