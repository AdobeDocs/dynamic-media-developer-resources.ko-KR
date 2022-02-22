---
title: pos
description: '디칼 위치 대상 vignette 개체에서 정의한 decal 원본 점까지의 오프셋(예: decal 이미지의 anchor= 점에서 인치)을 정의합니다.'
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 531f1465-2bec-46b6-a41e-54d993cbf410
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 4%

---

# pos{#pos}

디칼 위치 대상 vignette 개체에서 정의한 decal 원본 점까지의 오프셋(예: decal 이미지의 anchor= 점에서 인치)을 정의합니다.

`pos=x,y`

<table id="simpletable_DB3B64EFB67A47AD843812324ABFAE45"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>,<span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>장면 좌표 단위(일반적으로 인치)(실제, 실제)에서의 상대적 위치 조정. </p></td> 
 </tr> 
</table>

## 속성 {#section-50371cfa4e244bc49d2295a918749258}

재료 속성입니다. 십자가 이외의 물질에 의해 무시됨.

## 기본값 {#section-1b66efab054c45ca8d67d6a9865020f4}

`pos=0,0`. 비네팅 객체의 끝 원점에 비네팅 점을 맞춥니다.

## 참조 {#section-7cd8139481334ed79704d628b5bbd236}

[장면 좌표](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1), [앵커=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
