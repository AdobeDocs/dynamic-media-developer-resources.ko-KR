---
description: 광택 맵 이미지. 반복 가능한 텍스처, 배경 무늬/테두리 또는 디칼의 매끄러운 광택을 픽셀 단위로 제어할 수 있습니다.
seo-description: 광택 맵 이미지. 반복 가능한 텍스처, 배경 무늬/테두리 또는 디칼의 매끄러운 광택을 픽셀 단위로 제어할 수 있습니다.
seo-title: 매끄러운 지도
solution: Experience Manager
title: 매끄러운 지도
topic: Scene7 Image Serving - Image Rendering API
uuid: f137d362-74a1-45b3-9274-a3a2d6cf5db0
translation-type: tm+mt
source-git-commit: 515fcf8488eba7d9ca501a4182eaa73f1936488b
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 2%

---


# 매끄러운 맵{#glossmap}

광택 맵 이미지. 반복 가능한 텍스처, 배경 무늬/테두리 또는 디칼의 매끄러운 광택을 픽셀 단위로 제어할 수 있습니다.

`glossmap={ *``*| *`글로스맵 파일 포함Req`*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> embeddedReq</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">&amp;lbrash;'is&amp;<span class="varname"> lbradance;'isReq</span>'&amp;rbradance;'&amp;rbradance;|&amp;lbradance;'&amp;lbrasce;'<span class="varname"> foreignReq</span>'&amp;rbradance;'  </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> glossingMapFile</span> </span> </p></td> 
  <td class="stentry"> <p>광택 맵 이미지 파일(회색 음영). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> isReq</span> </span> </p></td> 
  <td class="stentry"> <p>이미지 서버에 요청. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> foreignReq  </span> </span> </p></td> 
  <td class="stentry"> <p>외부 서버에 요청. </p></td> 
 </tr> 
</table>

금속성 페인트 효과, die-cut Hole 벽지 및 테두리, 금속성 스레드 섬유 등의 재료에 적용됩니다.

광택 맵 이미지는 8비트 회색 음영이어야 하며 `src=`으로 지정된 기본 이미지와 정확히 크기가 같아야 합니다. 자세한 내용은 [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)의 설명을 참조하십시오.

## 속성 {#section-26375672d69849be9b026cc93c3bc558}

재료 속성. 반복 가능한 텍스처, 배경 무늬 및 테두리, 디캘이 지원합니다. 단색, 캐비닛 및 창을 덮는 재질이 무시되었습니다. 자세한 내용은 [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)을 참조하십시오.

## 기본값 {#section-d9ac031fb2f94482ac3fe2283d7cb168}

없음.

## 참조 {#section-33953fc1be82452da37141f2e541e00c}

[광택=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca),  [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
