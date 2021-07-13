---
description: 이미지 맵 데이터. 이 레이어의 이미지 맵 데이터를 제공합니다. 이 레이어의 카탈로그 맵에서 데이터를 무시합니다.
solution: Experience Manager
title: 맵
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7c1fbb50-98ec-4d9a-b608-93d60d687069
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 3%

---

# 맵{#map}

이미지 맵 데이터. 이 레이어의 이미지 맵 데이터를 제공합니다. 카탈로그에서 모든 데이터를 재정의합니다.:이 레이어에 대해 매핑합니다.

`map=[ *``*]mapA=[ *`stringA`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>이 레이어의 이미지 맵 데이터를 레이어 좌표로 표시합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> stringA</span></span> </p></td> 
  <td class="stentry"> <p>소스 이미지 좌표에서 이 레이어의 이미지 맵 데이터입니다. </p></td> 
 </tr> 
</table>

빈 문자열은 이 레이어가 이미지 맵을 제공하지 않아야 함을 나타냅니다. 구문 분석 문제를 방지하기 위해 문자열을 올바르게 HTTP로 인코딩해야 합니다.

*`string`*&#x200B;에서 발생하는 모든 앰퍼샌드(&amp;) 문자는 http로 인코딩해야 합니다.

`mapA=` 및 `catalog::Map` 은 소스 이미지 좌표에서 맵 데이터를 지정하는 반면, `map=` 는 레이어 사각형의 맨 위 왼쪽 모서리에 대한 레이어 좌표를 가정합니다( `rotate=` 및 `extend=` 가 적용된 후).

출력 이미지 맵은 항상 레이어 사각형으로 잘립니다. `shape` 속성을 생략하거나 `default` 로 설정하면 전체 레이어 사각형이 이미지 맵 영역으로 사용됩니다.

## 속성 {#section-a18d9ea95c71414a905a68b8839c0843}

레이어 속성입니다. `layer=comp`에 적용되면 지정된 맵 데이터가 다른 모든 이미지 맵 뒤에 레이어됩니다. `req=map` 이외의 경우는 무시됩니다. 효과 레이어에서 무시됨. `mapA=` 도 지정되 `map=` 는 경우 가 무시됩니다.

## 기본값 {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` 이 지정되지  `map=` 않은 경우 사용됩니다.

## 예 {#section-cd7691c94f984222845c86dcb0051ce8}

단순 텍스트 레이어의 사각형 이미지 맵을 정의합니다.

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

대부분(기본) 특성이 있는 `AREA` 요소는 전체 레이어 사각형에 대한 맵 영역을 삽입하는 데 사용됩니다.

## 참조 {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[이미지 맵](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab),  [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
