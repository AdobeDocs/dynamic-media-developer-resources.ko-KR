---
description: 색상 양자화. GIF 출력 변환의 색상 양자화 특성을 지정합니다.
solution: Experience Manager
title: 수량
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 71d59961-848e-4d78-875e-066e842ac1bf
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 3%

---

# 수량{#quantize}

색상 양자화. GIF 출력 변환의 색상 양자화 특성을 지정합니다.

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorcolorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 유형  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac}  </span> </p> <p>팔레트 유형을 지정합니다. </p> <p>이미지에 대한 최적 팔레트를 계산하려면 <span class="codeph"> 적응형 </span> 로 설정하십시오. </p> <p>사전 정의된 팔레트를 선택하려면 <span class="codeph"> web </span> 또는 <span class="codeph"> mac </span>로 설정하십시오. </p> <p> <p>참고: <span class="codeph"> mac </span> 팔레트 유형은 GIF 및 PNG8 형식에만 지원되지만 GIF-Alpha 및 PNG8-Alpha 형식에는 지원되지 않습니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> dither  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {diffuse|off}  </span> </p> <p>디더링 옵션을 지정합니다. </p> <p>Floyd-Steinberg 오류 확산용 <span class="codeph"> 확산 </span>으로 설정합니다. </p> <p>디더링을 비활성화하려면 </span>을 <span class="codeph">으로 설정하십시오. </span></p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> </p> </td> 
   <td colname="col2"> <p>출력 색상 수(2-256) </p> <p><span class="codeph"> 적응형 </span> 팔레트에 포함되는 색상의 수를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> colorList  </span> </span> </p> </td> 
   <td colname="col2"> <p>16진수6 형식의 강제 RGB 색상의 쉼표로 구분된 목록 </p> <p><span class="codeph"> 적응형 </span> 팔레트에 포함할 색상을 지정할 수 있도록 해줍니다. 지정된 색상 수가 <span class="codeph"> <span class="varname"> numColors </span> </span>보다 작으면 이미지 내용에 따라 추가 색상이 계산됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-8ab5035055b24b858270d260912a7f3d}

요청 속성입니다. 현재 레이어 설정에 관계없이 적용됩니다. `fmt=gif`, `fmt=gif-alpha`, `fmt=png8` 또는 `fmt=png8-alpha`인 경우에만 사용됩니다. 그렇지 않으면 무시됩니다.

`*`colorList`*`에 지정된 색상은 &#39; `0x`&#39; 접두사가 없는 16진수6 형식의 RGB 값으로 구성되어야 합니다(` [color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423)` 참조). 다른 색상 지정자는 허용되지 않습니다. *`numColors`* 는 2-256 사이여야 합니다.

## 기본값 {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## 예 {#section-e34aca7587d548a7ae9d4266b80c9451}

`web` 팔레트를 사용하여 GIF 축소판을 생성하고 디더링을 수행하지 않습니다.

` http:// *`서버`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

키 색상 투명도와 힘 색상을 흑백으로 사용하여 이미지를 두 가지 색조 GIF로 변환합니다.

` http:// *`서버`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## 참조 {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ,  [색상](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
