---
description: 레이어 원점
seo-description: 레이어 원점
seo-title: 기원
solution: Experience Manager
title: 기원
topic: Scene7 Image Serving - Image Rendering API
uuid: a36fc0b6-7744-4c1c-b9f8-4aa31a886bff
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 기원{#origin}

레이어 원점

`origin= *`coord`*`

`originN= *`coordN`*`

<table id="simpletable_A270FD92B1E841FE81F5AB300351FE01"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p></td> 
  <td class="stentry"> <p>레이어 사각형의 왼쪽 위 모퉁이에서 픽셀 오프셋(int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>레이어 사각형의 중심에서 표준화된 오프셋(실제, 실제). </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>The layer rect always includes any modification by `extend=`.

레이어 사각형의 정렬 점을 정의합니다. 이 점은 레이어 0을 통해 레이어 사각형을 기준으로 위치를 지정하는 데 사용됩니다 `pos=`. `originN=0,0` 레이어 원점을 레이어 사각형 가운데에 배치합니다. `originN=-0.5,-0.5` 왼쪽 `origin=0,0` 위 모서리이고 레이어 사각형의 오른쪽 아래 `originN=0.5,0.5` 모퉁이입니다.

## 속성 {#section-60f639e36ada43d1abc6bfc100afc925}

레이어 특성. 현재 레이어나 레이어 0에 적용되는 경우 `layer=comp`입니다. 레이어 소스에 적용된 레이어 변형(, `crop=`, `scale=``rotate=`, `flip=`)의 영향을 받지 않습니다. Overrides `anchor=`. 효과 레이어에서 무시됩니다.

## 기본값 {#section-b7209e5c2ad6491fb0c2353cc3f1f703}

지정하지 `origin=` 않으면 레이어 원점이 이미지 앵커에 레이어 변형을 적용하여 결정됩니다. 이미지 앵커를 알 수 없으면 레이어 사각형( `originN=0,0`)의 중심이 사용됩니다.

## 예 {#section-13e38d6e17be4e6cbc6b27fbde63b291}

템플릿의 예 A를 [참조하십시오](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## 참조 {#section-a9f9c42c86fe45798deb2daaf27ea5b7}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) , [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143), [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
