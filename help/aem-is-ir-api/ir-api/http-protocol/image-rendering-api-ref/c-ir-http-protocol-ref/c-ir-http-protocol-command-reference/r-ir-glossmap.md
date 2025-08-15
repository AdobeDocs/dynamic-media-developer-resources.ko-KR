---
title: glossmap
description: 광택 맵 이미지입니다. 반복 가능한 텍스처, 배경 무늬/테두리 또는 데칼의 광택을 픽셀별로 제어합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 922fc527-be19-4d7a-b265-7bdb1de80990
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 2%

---

# glossmap {#glossmap}

광택 맵 이미지입니다. 반복 가능한 텍스처, 배경 무늬/테두리 또는 데칼의 광택을 픽셀별로 제어합니다.

`glossmap={ *`glossMapFile`*| *`embeddedReq`*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> embeddedReq</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">&amp;lbrace;'is&amp;lbrace;'<span class="varname"> isReq</span>'&amp;rbrace;'&amp;rbrace;|&amp;lbrace;'&amp;lbrace;'&amp;lbrace;'<span class="varname"> foreignReq</span>'&amp;rbrace;' </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> glossMapFile</span> </span> </p></td> 
  <td class="stentry"> <p>광택 맵 이미지 파일(회색 음영). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> isReq</span> </span> </p></td> 
  <td class="stentry"> <p>이미지 서버에 요청합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> foreignReq </span> </span> </p></td> 
  <td class="stentry"> <p>외부 서버에 요청합니다. </p></td> 
 </tr> 
</table>

금속 페인트 효과, 다이 컷 호일 배경 화면 및 테두리, 금속 실 직물과 같은 소재에 적용 할 수 있습니다.

광택 맵 이미지는 8비트 회색조여야 하며 `src=`(으)로 지정된 기본 이미지와 크기가 같아야 합니다. 자세한 내용은 [`gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)의 설명을 참조하세요.

## 속성 {#section-26375672d69849be9b026cc93c3bc558}

재질 속성입니다. 반복 가능한 텍스처, 배경 화면 및 테두리, 데칼에서 지원됩니다. 단색, 캐비닛 및 창 덮개 재료에서 무시됩니다. 자세한 내용은 [`gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)을(를) 참조하십시오.

## 기본값 {#section-d9ac031fb2f94482ac3fe2283d7cb168}

없음.

## 참조 {#section-33953fc1be82452da37141f2e541e00c}

[글로스=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca), [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
