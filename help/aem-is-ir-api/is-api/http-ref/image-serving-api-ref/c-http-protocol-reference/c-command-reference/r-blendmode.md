---
description: 혼합 모드. 레이어를 합성할 때 사용되는 혼합 유형을 지정합니다. Photoshop에서 사용할 수 있는 일반적으로 사용되는 혼합 모드를 시뮬레이션합니다. 자세한 내용은 Photoshop 설명서를 참조하십시오.
seo-description: 혼합 모드. 레이어를 합성할 때 사용되는 혼합 유형을 지정합니다. Photoshop에서 사용할 수 있는 일반적으로 사용되는 혼합 모드를 시뮬레이션합니다. 자세한 내용은 Photoshop 설명서를 참조하십시오.
seo-title: blendMode
solution: Experience Manager
title: blendMode
topic: Scene7 Image Serving - Image Rendering API
uuid: 9ae30495-c10b-4c55-968e-effb602a0857
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 14%

---


# blendMode{#blendmode}

혼합 모드. 레이어를 합성할 때 사용되는 혼합 유형을 지정합니다. Photoshop에서 사용할 수 있는 일반적으로 사용되는 혼합 모드를 시뮬레이션합니다. 자세한 내용은 Photoshop 설명서를 참조하십시오.

`blendMode=norm|dissolve|lighten|darken|mult|screen`

## 속성 {#section-418aad5a417f49929d1953e226e5c8dd}

레이어 속성을 참조하십시오. `layer=0` 및 `layer=comp`에서 무시됩니다.

## 기본값 {#section-69829acc6532448d8612a4a54e86f00e}

`blendMode=norm`

## 예 {#section-d209dd9c270b469c87558a8910c50b61}

`…&size=200,200&bgColor=191,120,241&…`

`…&layer=1&src=myRootId/myImageId&opac=80&blendMode=dissolve&…`

## 참조 {#section-bc7ccdfcb310441c938c0bde3e00d7b3}

[opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5)
