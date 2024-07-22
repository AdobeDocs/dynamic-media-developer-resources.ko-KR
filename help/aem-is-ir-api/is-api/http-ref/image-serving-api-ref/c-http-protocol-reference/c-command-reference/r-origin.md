---
title: 원본
description: 레이어 원점.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5ea8eb18-d169-4255-b4b1-dda849246485
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 2%

---

# 원본{#origin}

레이어 원점.

`origin= *`명령`*`

`originN= *`coordN`*`

<table id="simpletable_A270FD92B1E841FE81F5AB300351FE01"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 열</span> </p></td> 
  <td class="stentry"> <p>레이어 rect의 왼쪽 위 모서리에서 픽셀 오프셋(int, int)입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>레이어 rect(실수, 실수)의 중심에서 정규화된 오프셋입니다. </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>레이어 rect에는 `extend=`에 의한 수정 내용이 항상 포함됩니다.

`pos=`을(를) 통해 레이어 0을 기준으로 레이어 사각형을 배치하는 데 사용되는 레이어 사각형의 정렬 지점을 정의합니다. `originN=0,0`은(는) 레이어 사각형의 중심에 레이어 원점을 배치합니다. `originN=-0.5,-0.5` 및 `origin=0,0`은(는) 왼쪽 위 모서리이고 `originN=0.5,0.5`은(는) 레이어 사각형의 오른쪽 아래 모서리입니다.

## 속성 {#section-60f639e36ada43d1abc6bfc100afc925}

레이어 속성입니다. `layer=comp`인 경우 현재 레이어 또는 레이어 0에 적용됩니다. 레이어 소스에 적용된 레이어 변형( `crop=`, `scale=`, `rotate=`, `flip=`)의 영향을 받지 않습니다. `anchor=`을(를) 재정의합니다. 효과 레이어에서 무시됨.

## 기본값 {#section-b7209e5c2ad6491fb0c2353cc3f1f703}

`origin=`을(를) 지정하지 않으면 이미지 앵커에 레이어 변형을 적용하여 레이어 원점을 결정합니다. 이미지 앵커를 알 수 없는 경우 레이어 사각형의 가운데(`originN=0,0`)가 사용됩니다.

## 예 {#section-13e38d6e17be4e6cbc6b27fbde63b291}

[템플릿](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)에서 예제 A를 참조하십시오.

## 참조 {#section-a9f9c42c86fe45798deb2daaf27ea5b7}

[앵커=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) , [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143), [확장=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
