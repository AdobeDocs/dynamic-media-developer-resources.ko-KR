---
title: 맵
description: 이미지 맵 데이터. 이 레이어에 대한 이미지 맵 데이터를 제공합니다. 이 레이어에 대해 카탈로그 맵의 데이터를 무시합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7c1fbb50-98ec-4d9a-b608-93d60d687069
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 2%

---

# 맵{#map}

이미지 맵 데이터. 이 레이어에 대한 이미지 맵 데이터를 제공합니다. 이 레이어에 대해 catalog::Map의 모든 데이터를 무시합니다.

`map=[ *`문자열`*]mapA=[ *`문자열A`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 문자열</span></span> </p></td> 
  <td class="stentry"> <p>레이어 좌표로 이 레이어의 이미지 맵 데이터입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> stringA</span></span> </p></td> 
  <td class="stentry"> <p>소스 이미지 좌표에서 이 레이어의 이미지 맵 데이터입니다. </p></td> 
 </tr> 
</table>

빈 문자열은 이 레이어가 이미지 맵을 제공하지 않아야 함을 나타냅니다. 구문 분석 문제를 방지하려면 문자열이 올바르게 HTTP 인코딩되어야 합니다.

*`string`*&#x200B;에서 발생하는 모든 앰퍼샌드(&amp;) 문자는 http 인코딩이 적용되어야 합니다.

`mapA=` 및 `catalog::Map`은(는) 맵 데이터를 소스 이미지 좌표로 지정하지만 `map=`은(는) 레이어 사각형의 위쪽, 왼쪽 모퉁이를 기준으로 레이어 좌표를 가정합니다(`rotate=` 및 `extend=`이(가) 적용된 후).

출력 이미지 맵은 항상 레이어 사각형에 클리핑됩니다. `shape` 특성을 생략하거나 `default`(으)로 설정하면 전체 레이어 사각형이 이미지 맵 영역으로 사용됩니다.

## 속성 {#section-a18d9ea95c71414a905a68b8839c0843}

레이어 속성입니다. `layer=comp`에 적용하면 지정된 맵 데이터가 다른 모든 이미지 맵 뒤에 계층화됩니다. `req=map`이(가) 아니면 무시됩니다. 효과 레이어에서 무시됨. `mapA=`도 지정된 경우 `map=`이(가) 무시됩니다.

## 기본값 {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map`이(가) 지정되지 않은 경우 `map=`이(가) 사용됩니다.

## 예 {#section-cd7691c94f984222845c86dcb0051ce8}

간단한 텍스트 레이어에 대해 사각형 이미지 맵을 정의합니다.

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

(대부분) 기본 특성이 있는 `AREA` 요소는 전체 레이어 사각형에 대한 맵 영역을 삽입하는 데 사용됩니다.

## 참조 {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[이미지 맵](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab), [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
