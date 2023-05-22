---
description: 이미지 불투명도를 조정합니다. 이미지, 텍스트, 단색 또는 효과 레이어의 전경 불투명도를 줄일 수 있습니다.
solution: Experience Manager
title: opac
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38e0e1dc-46c0-48a4-b676-f7e6d262392f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 1%

---

# opac{#opac}

이미지 불투명도를 조정합니다. 이미지, 텍스트, 단색 또는 효과 레이어의 전경 불투명도를 줄일 수 있습니다.

`opac= *`불투명도`*[, *`fillOpacity`*]`

<table id="simpletable_DA4B5D86C496480886FADB284AD6047F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 불투명도</span> </p> </td> 
  <td class="stentry"> <p>기본 불투명도(0...100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> fillOpacity</span> </p></td> 
  <td class="stentry"> <p>채우기 불투명도(0...100 int). </p></td> 
 </tr> 
</table>

이미지 레이어의 전경 불투명도는 레이어 마스크 또는 이미지의 알파 채널에 의해 결정되거나, 둘 다 없는 경우에는 100%입니다. 텍스트 레이어의 전경 불투명도는 100%이고 단색 레이어의 불투명도는 `color=`.

`opac=` 칠해진 영역의 불투명도는 수정하지 않습니다. `color=` 또는 `bgColor=`단색 및 효과 레이어의 전경 영역 제외( `color=`).

이미지, 텍스트 또는 단색 레이어에 지정된 경우 *`opacity`* 에서는 연결된 모든 효과 레이어를 포함하여 전체 레이어를 적용하며 *`fillOpacity`* 기본 레이어 콘텐츠에만 적용됩니다. 효과 레이어에 지정된 경우 *`opacity`* 이 효과 레이어에 적용되는 반면 *`fillOpacity`* 은(는) 무시됩니다.

기본 레이어 내용에 대한 유효한 불투명도는 ( *`opacity`* &#42; *`fillOpacity`* / 100). 효과 레이어의 유효한 불투명도는 (주 *`opacity`* &#42; 효과 *`opacity`* / 100).

## 속성 {#section-ac3f136ff1584a2eab87500b7164f7fa}

레이어 속성입니다. 다음과 같은 경우 현재 레이어 또는 합성 이미지에 적용됩니다. `layer=comp`.

## 기본값 {#section-abba67ed028049048ae43405ea69b164}

`opac=100,100`레이어 불투명도를 변경하지 않는 경우입니다.

## 예 {#section-9710810e96af40538652e8ae4aadd3be}

… `&layer=1&text=variable%20opacity&opac=90,70&effect=-1&opac=50&`…

이 예제의 텍스트 불투명도는 90입니다&#42;70/100=63%, 효과 레이어 불투명도는 90입니다&#42;50/100=45%.

## 참조 {#section-dbdad35ccd544590b4b11d31a9ab062e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)
