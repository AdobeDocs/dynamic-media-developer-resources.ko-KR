---
description: 그라우트 색상 및 두께를 바둑판식으로 배열합니다. 세라믹 및 천연 돌타일에 대한 그루트를 시뮬레이션합니다.
seo-description: 그라우트 색상 및 두께를 바둑판식으로 배열합니다. 세라믹 및 천연 돌타일에 대한 그루트를 시뮬레이션합니다.
seo-title: 그루트
solution: Experience Manager
title: 그루트
topic: Scene7 Image Serving - Image Rendering API
uuid: 00069004-40f2-4ab6-85d8-ca197b7bef69
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 2%

---


# grout{#grout}

그라우트 색상 및 두께를 바둑판식으로 배열합니다. 세라믹 및 천연 돌타일에 대한 그루트를 시뮬레이션합니다.

grout= *`color`*[,*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> color  </span> </span> </p> </td> 
  <td class="stentry"> <p>그루트 색상(회색 또는 RGB). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td> 
  <td class="stentry"> <p>그라우트 두께;장면 좌표 단위(일반적으로 인치)(실제). </p> </td> 
 </tr> 
</table>

그룹 외양을 최대한 제어하려면 다음 요구 사항이 적용됩니다.

* 타일은 정사각형 또는 직사각형이어야 합니다.현재 다른 모양은 지원되지 않습니다.
* 이미지에는 단일 타일만 포함되어야 합니다.
* 이미지의 기본 그룹(있는 경우)은 4개의 모든 가장자리에 정확히 동일한 두께를 가져야 합니다.
* 기본 그룹의 두께는 재료 카탈로그( `catalog::GroutWidth`)에 지정해야 합니다.

## 속성 {#section-de78b678245b4ffda48097c345949e77}

재료 속성. ` *`색상`*` 은 RGB 색상 값이어야 합니다. ` *`너비`*` 는 실제 값 0 이상이어야 합니다.

반복 가능한 텍스처가 아닌 재질에 대해 반복 = 4, 5, 7, 8, 9, 14 이상이 지정되면 무시됩니다.

## 기본값 {#section-bfab3621f70b4489a21994ab11b20cc6}

`grout=`을(를) 지정하지 않으면 이미지의 그룹이 수정되지 않습니다. ` grout= *`color`*`이 지정된 경우 ` *`width`*`의 기본값은 `catalog::GroutWidth`입니다.

## 참조 {#section-8d472906a44943f5a8557e98f2fbc71f}

[색상 값](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
