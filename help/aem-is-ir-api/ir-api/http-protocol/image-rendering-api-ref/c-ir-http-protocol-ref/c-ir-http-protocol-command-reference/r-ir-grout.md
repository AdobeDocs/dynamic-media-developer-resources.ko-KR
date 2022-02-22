---
title: 그루트
description: 타일 그라우트 색상 및 두께. 세라믹 및 천연 돌 타일에 대한 그루트를 시뮬레이션합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6647b459-11d2-47e4-9033-3a740f01a623
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 3%

---

# 그루트 {#grout}

타일 그라우트 색상 및 두께. 세라믹 및 천연 돌 타일에 대한 그루트를 시뮬레이션합니다.

grout= *`color`*[,*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 색상 </span> </span> </p> </td>
  <td class="stentry"> <p>색상(회색 또는 RGB) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td>
  <td class="stentry"> <p>굵기; 장면 좌표 단위(일반적으로 인치)(실제). </p> </td>
 </tr> 
</table>

그룹 모양을 최대한 제어하려면 다음 요구 사항이 적용됩니다.

* 타일은 정사각형 또는 직사각형이어야 합니다. 현재 지원되는 다른 셰이프는 없습니다.
* 이미지에는 단일 타일만 포함해야 합니다.
* 이미지의 기본 그룹(있는 경우)은 4개의 가장자리 모두에서 동일한 두께를 가져야 합니다.
* 기본 그룹의 두께는 재료 카탈로그에서 지정해야 합니다( `catalog::GroutWidth`).

## 속성 {#section-de78b678245b4ffda48097c345949e77}

재료 속성입니다. `*`색상`*` RGB 색상 값이어야 합니다. `*`너비`*` 는 실제 값 0보다 커야 합니다.

반복 가능한 텍스처가 아닌 재질에 대해 반복 = 4, 5, 7, 8, 9, 14 이상이거나 반복 가능한 텍스처가 지정된 경우 무시됩니다.

## 기본값 {#section-bfab3621f70b4489a21994ab11b20cc6}

If `grout=` 가 지정되지 않은 경우 이미지의 그룹이 수정되지 않습니다. If `grout= *`색상`*` 지정한 경우 `*`너비`*` 기본값은 입니다. `catalog::GroutWidth`.

## 참조 {#section-8d472906a44943f5a8557e98f2fbc71f}

[색상 값](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
