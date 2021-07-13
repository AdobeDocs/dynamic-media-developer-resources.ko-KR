---
description: 비네팅 파일입니다. 이 요청에 사용할 비네팅을 지정합니다.
solution: Experience Manager
title: vignett
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8419d68d-7579-4e62-abbd-7dc0a736ae23
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 4%

---

# vignett{#vignette}

비네팅 파일입니다. 이 요청에 사용할 비네팅을 지정합니다.

`vignette=[ *``*/] *``*|[catId/] *`catIdrecIdfile`*`

<table id="simpletable_432EC5501CA3431B83A762C3EE4E8DD2"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p> </td> 
  <td class="stentry"> <p>재료 카탈로그 ID(<span class="codeph"> 속성과 일치함::RootId</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>비네팅 ID(<span class="codeph"> 비네팅::Id</span>)에 일치함. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 파일</span> </p></td> 
  <td class="stentry"> <p>상대 비네팅 파일 경로 및 이름입니다. </p></td> 
 </tr> 
</table>

비네팅 맵 항목이나 비네팅 파일을 지정할 수 있습니다. 원격 URL은 허용되지 않습니다.

`vignette=` 는 요청 URL 경로에서 비네팅을 지정하는 대신 사용할 수 있습니다. 주로 템플릿의 변수를 통해 비네팅을 지정하는 데 사용됩니다.

*`catId`*&#x200B;을 지정하지 않으면 세션 카탈로그가 사용됩니다.

## 속성 {#section-f58661fc78d7496e8e3d0fb98b945c4b}

요청 내 어디에서나 발생할 수 있습니다. 요청 URL 경로로 지정된 비네팅을 무시합니다.

## 기본값 {#section-db0618d48bc84dc8abcc989550349ccc}

없음.

## 참조 {#section-dc2668cc2cd54a74b08cff68a12d4edd}

[재료 카탈로그](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2),  [사용자 지정 변수](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-custom-variables/c-ir-custom-variables.md#concept-8a1d9a50d09a4b7b97b8c83365971f96)
