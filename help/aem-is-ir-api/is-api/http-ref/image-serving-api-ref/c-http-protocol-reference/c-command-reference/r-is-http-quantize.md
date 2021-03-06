---
title: 수량
description: 색상 양자화. GIF 출력 변환에 대한 색상 양자화 특성을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71d59961-848e-4d78-875e-066e842ac1bf
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 3%

---

# 수량{#quantize}

색상 양자화. GIF 출력 변환에 대한 색상 양자화 특성을 지정합니다.

` quantize= *`유형`*[, *`dither`*[, *`numColors`*[, *`colorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 유형 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac} </span> </p> <p>팔레트 유형을 지정합니다. </p> <p>을 로 설정합니다. <span class="codeph"> 적응형 </span> 를 입력하여 이미지에 대한 최적 팔레트를 계산합니다. </p> <p>을 로 설정합니다. <span class="codeph"> 웹 </span> 또는 <span class="codeph"> mac </span> 사전 정의된 팔레트를 선택합니다. </p> <p> <p>참고: 다음 <span class="codeph"> mac </span> 팔레트 유형은 GIF 및 PNG8 형식에만 지원되지만 GIF-알파 및 PNG8-Alpha 형식에는 지원되지 않습니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> dither </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {diffuse|off} </span> </p> <p>디더링 옵션을 지정합니다. </p> <p>을 로 설정합니다. <span class="codeph"> 확산 </span> Floyd-Steinberg 오류 확산용 </p> <p>을 로 설정합니다. <span class="codeph"> 해제 </span> 디더링을 비활성화합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
   <td colname="col2"> <p>출력 색상 수(2-256) </p> <p>에 포함되는 색상의 수를 지정합니다 <span class="codeph"> 적응형 </span> 팔레트. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> colorList </span> </span> </p> </td> 
   <td colname="col2"> <p>16진수6 형식의 강제 RGB 색상의 쉼표로 구분된 목록 </p> <p>에 포함할 색상을 지정할 수 있습니다 <span class="codeph"> 적응형 </span> 팔레트. 지정한 색상 수가 <span class="codeph"> <span class="varname"> numColors </span> </span>을 지정하면 이미지 컨텐츠를 기반으로 추가 색상이 계산됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-8ab5035055b24b858270d260912a7f3d}

요청 속성입니다. 현재 레이어 설정에 관계없이 적용됩니다. 다음 경우에만 사용됩니다 `fmt=gif`, `fmt=gif-alpha`, `fmt=png8`, 또는 `fmt=png8-alpha`. 그렇지 않으면 무시됩니다.

지정한 색상 *`colorList`* 는 hex6 형식의 RGB 값으로 구성되어야 합니다(참조) [색상](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md) 사용 안 함 `0x` 접두사를 사용합니다. 다른 색상 지정자는 허용되지 않습니다. *`numColors`* 는 2-256 사이여야 합니다.

## 기본값 {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## 예 {#section-e34aca7587d548a7ae9d4266b80c9451}

를 사용하여 GIF 축소판 생성 `web` 팔레트 및 디더링 없음:

` http:// *`서버`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

이미지를 키 색상 투명도가 있는 두 가지 색조 GIF으로 변환하고 색상을 흑백으로 변환합니다.

` http:// *`서버`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## 참조 {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [색상](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
