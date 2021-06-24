---
description: 광택 맵 이미지입니다. 반복 가능한 텍스쳐, 월페이퍼/테두리 또는 십자의 광택도를 픽셀 단위로 제어할 수 있습니다.
solution: Experience Manager
title: 광택 맵
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 922fc527-be19-4d7a-b265-7bdb1de80990
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 3%

---

# 광택 맵{#glossmap}

광택 맵 이미지입니다. 반복 가능한 텍스쳐, 월페이퍼/테두리 또는 십자의 광택도를 픽셀 단위로 제어할 수 있습니다.

`glossmap={ *``*| *`glotsMapFileembeddedReq`*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> embeddedReq</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">&amp;lbrase;'is&amp;lbrase;'<span class="varname"> isReq</span>'&amp;rbrase;'&amp;rbrase;|&amp;lbrase;'&amp;lbrase;'<span class="varname"> foreignReq</span>'&amp;rbrases;'  </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> gloseMapFile</span> </span> </p></td> 
  <td class="stentry"> <p>광택 맵 이미지 파일(회색 음영). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> isReq</span> </span> </p></td> 
  <td class="stentry"> <p>이미지 서버에 요청합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> foreignReq  </span> </span> </p></td> 
  <td class="stentry"> <p>외부 서버에 요청합니다. </p></td> 
 </tr> 
</table>

금속 페인트 효과, 금속성 박판 및 테두리, 금속성 실 섬유 등의 재료에 적용 가능하다.

광택 맵 이미지는 8비트 회색 음영이어야 하며 `src=`에 지정된 1차 이미지와 정확히 동일한 크기를 가져야 합니다. 자세한 내용은 [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)의 설명을 참조하십시오.

## 속성 {#section-26375672d69849be9b026cc93c3bc558}

재료 속성입니다. 반복 가능한 텍스처, 벽지 및 테두리, 디칼에서 지원됩니다. 단색, 캐비닛 및 창 덮개에 의해 무시됩니다. 자세한 내용은 [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) 을 참조하십시오.

## 기본값 {#section-d9ac031fb2f94482ac3fe2283d7cb168}

없음.

## 참조 {#section-33953fc1be82452da37141f2e541e00c}

[광택=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca),  [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
