---
title: 블렌드 모드
description: 혼합 모드. 레이어를 합성할 때 사용되는 혼합 유형을 지정합니다. Photoshop에서 일반적으로 사용되는 혼합 모드를 시뮬레이트합니다. 자세한 내용은 Photoshop 설명서 를 참조하십시오.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8f0b8b0a-a8ac-4932-986c-5d14d3311f1b
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 5%

---

# 블렌드 모드{#blendmode}

혼합 모드. 레이어를 합성할 때 사용되는 혼합 유형을 지정합니다. Photoshop에서 일반적으로 사용되는 혼합 모드를 시뮬레이트합니다. 자세한 내용은 Photoshop 설명서 를 참조하십시오.

`blendMode=norm|dissolve|lighten|darken|mult|screen`

## 속성 {#section-418aad5a417f49929d1953e226e5c8dd}

레이어 속성. `layer=0` 및 `layer=comp`이(가) 무시합니다.

## 기본값 {#section-69829acc6532448d8612a4a54e86f00e}

`blendMode=norm`

## 예 {#section-d209dd9c270b469c87558a8910c50b61}

`…&size=200,200&bgColor=191,120,241&…`

`…&layer=1&src=myRootId/myImageId&opac=80&blendMode=dissolve&…`

## 참조 {#section-bc7ccdfcb310441c938c0bde3e00d7b3}

[opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5)
