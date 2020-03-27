---
description: 이미지 맵 데이터를 참조하십시오. 이 레이어의 이미지 맵 데이터를 제공합니다. 이 레이어에 대한 카탈로그 맵의 데이터를 무시합니다.
seo-description: 이미지 맵 데이터를 참조하십시오. 이 레이어의 이미지 맵 데이터를 제공합니다. 이 레이어에 대한 카탈로그 맵의 데이터를 무시합니다.
seo-title: 맵
solution: Experience Manager
title: 맵
topic: Scene7 Image Serving - Image Rendering API
uuid: 9c1c3323-21ab-4820-bf4e-761b82ada1ab
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 맵{#map}

이미지 맵 데이터를 참조하십시오. 이 레이어의 이미지 맵 데이터를 제공합니다. 카탈로그::Map에서 이 레이어에 대한 모든 데이터를 무시합니다.

`map=[ *``*]mapA=[ *`stringA`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 문자열</span></span> </p></td> 
  <td class="stentry"> <p>레이어 좌표의 이 레이어에 대한 이미지 맵 데이터입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 문자열 <span class="varname"> A</span></span> </p></td> 
  <td class="stentry"> <p>소스 이미지 좌표의 이 레이어에 대한 이미지 맵 데이터입니다. </p></td> 
 </tr> 
</table>

빈 문자열은 이 레이어가 이미지 맵을 제공하지 않아야 함을 나타냅니다. 구문 분석 문제를 방지하려면 문자열이 HTTP로 제대로 인코딩되어야 합니다.

에서 발생하는 모든 앰퍼샌드(&amp;) 문자는 http 인코딩되어야 *`string`* 합니다.

소스 이미지 좌표에 맵 데이터를 `mapA=` 지정하고 지정하는 동안 레이어 사각형의 상단, 왼쪽 모서리를 기준으로 레이어 좌표를 `catalog::Map` 가정할 수 있습니다(적용 후 `map=``rotate=` `extend=` ).

출력 이미지 맵은 항상 레이어 사각형으로 잘립니다. 이 `shape` `default`속성을 생략하거나 로 설정하면 전체 레이어 사각형이 이미지 맵 영역으로 사용됩니다.

## 속성 {#section-a18d9ea95c71414a905a68b8839c0843}

레이어 특성. 에 `layer=comp`적용하면 지정된 맵 데이터가 다른 모든 이미지 맵 뒤에 레이어로 만들어집니다. 그렇지 않으면 `req=map`무시됩니다. 효과 레이어에서 무시됩니다. `mapA=` 도 `map=` 지정되면 무시됩니다.

## 기본값 {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` 이 사용되지 `map=` 않으면 사용됩니다.

## 예 {#section-cd7691c94f984222845c86dcb0051ce8}

간단한 텍스트 레이어의 사각형 이미지 맵을 정의합니다.

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

기본 속성이 대부분 있는 `AREA` 요소는 전체 레이어 사각형에 대한 맵 영역을 삽입하는 데 사용됩니다.

## 참조 {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[이미지 맵](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab), [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
