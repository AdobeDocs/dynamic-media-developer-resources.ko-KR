---
description: 레이어 원점.
seo-description: 레이어 원점.
seo-title: 기원
solution: Experience Manager
title: 기원
topic: Scene7 Image Serving - Image Rendering API
uuid: a36fc0b6-7744-4c1c-b9f8-4aa31a886bff
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 3%

---


# 원본{#origin}

레이어 원점.

`origin= *`coord`*`

`originN= *`coordN`*`

<table id="simpletable_A270FD92B1E841FE81F5AB300351FE01"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p></td> 
  <td class="stentry"> <p>레이어 사각형 왼쪽 위 모서리에서 픽셀 오프셋(int, int)을 만듭니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>레이어 사각형 중심으로부터 정규화된 오프셋(실제, 실제)입니다. </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>레이어는 항상 `extend=`의 수정을 포함합니다.

`pos=`을(를) 통해 레이어 0을 기준으로 레이어 사각형을 배치하는 데 사용되는 레이어 사각형의 정렬 점을 정의합니다. `originN=0,0` 레이어 원점을 레이어 사각형의 중앙에 배치합니다. `originN=-0.5,-0.5` 왼쪽 위 모서리 `origin=0,0` 에 있고 레이어 사각형 `originN=0.5,0.5` 의 오른쪽 아래 모서리입니다.

## 속성 {#section-60f639e36ada43d1abc6bfc100afc925}

레이어 속성입니다. 현재 레이어나 `layer=comp`인 경우 레이어 0에 적용됩니다. 레이어 소스에 적용된 레이어 변형( `crop=`, `scale=`, `rotate=`, `flip=`)의 영향을 받지 않습니다. `anchor=`을(를) 무시합니다. 효과 레이어에서 무시됩니다.

## 기본값 {#section-b7209e5c2ad6491fb0c2353cc3f1f703}

`origin=`을(를) 지정하지 않으면 레이어 변환을 이미지 앵커에 적용하여 레이어 원점을 결정합니다. 이미지 앵커를 알 수 없으면 레이어 사각형( `originN=0,0`)의 중심이 사용됩니다.

## 예 {#section-13e38d6e17be4e6cbc6b27fbde63b291}

[템플릿](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)의 예 A를 참조하십시오.

## 참조 {#section-a9f9c42c86fe45798deb2daaf27ea5b7}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) ,  [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143),  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
