---
title: 그라우트
description: 타일 그라우트 색상 및 두께입니다. 세라믹 및 천연 석재 타일의 그라우트를 시뮬레이션합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6647b459-11d2-47e4-9033-3a740f01a623
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 2%

---

# 그라우트 {#grout}

타일 그라우트 색상 및 두께입니다. 세라믹 및 천연 석재 타일의 그라우트를 시뮬레이션합니다.

grout= *`color`*[,*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 색상 </span> </span> </p> </td>
  <td class="stentry"> <p>그라우트 색상(회색 또는 RGB) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td>
  <td class="stentry"> <p>그라우트 두께, 장면 좌표 단위(일반적으로 인치)(실수) </p> </td>
 </tr> 
</table>

그라우트 모양을 최대한 제어하려면 다음 요구 사항이 적용됩니다.

* 타일은 정사각형 또는 직사각형이어야 하며 현재 다른 모양이 지원되지 않습니다.
* 이미지에는 단일 타일만 포함되어야 합니다.
* 이미지의 기본 그라우트(있는 경우)는 네 개의 모든 모서리에서 두께가 같아야 합니다.
* 기본 그라우트의 두께는 재료 카탈로그( `catalog::GroutWidth`).

## 속성 {#section-de78b678245b4ffda48097c345949e77}

재질 속성입니다. `*`색상`*` RGB 색상 값이어야 합니다. `*`폭`*` 은(는) 실수 값 0 이상이어야 합니다.

반복 = 4, 5, 7, 8, 9, 14 이상인 경우 또는 반복 가능한 질감 이외의 재료에 대해 지정된 경우 무시됩니다.

## 기본값 {#section-bfab3621f70b4489a21994ab11b20cc6}

If `grout=` 이 지정되지 않은 경우 이미지의 그루트가 수정되지 않습니다. If `grout= *`색상`*` 을(를) 지정했습니다. `*`폭`*` 기본값은 입니다. `catalog::GroutWidth`.

## 참조 {#section-8d472906a44943f5a8557e98f2fbc71f}

[색상 값](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
