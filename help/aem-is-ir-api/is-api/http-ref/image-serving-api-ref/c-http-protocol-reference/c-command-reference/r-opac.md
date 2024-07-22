---
title: opac
description: 이미지 불투명도를 조정합니다. 이미지, 텍스트, 단색 또는 효과 레이어의 전경 불투명도를 줄일 수 있습니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38e0e1dc-46c0-48a4-b676-f7e6d262392f
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '226'
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

이미지 레이어의 전경 불투명도는 레이어 마스크 또는 이미지의 알파 채널에 의해 결정되거나, 둘 다 없는 경우에는 100%입니다. 텍스트 레이어의 전경 불투명도는 100%이고 단색 레이어의 불투명도는 `color=`에 의해 설정됩니다.

`opac=`은(는) 단색 및 효과 레이어(`color=`)의 전경 영역을 제외하고 `color=` 또는 `bgColor=`(으)로 채워진 영역의 불투명도를 수정하지 않습니다.

이미지, 텍스트 또는 단색 레이어에 지정된 경우 *`opacity`*&#x200B;은(는) 연결된 모든 효과 레이어를 포함하여 전체 레이어를 적용하고 *`fillOpacity`*&#x200B;은(는) 기본 레이어 콘텐츠에만 적용됩니다. 효과 레이어에 지정하면 *`opacity`*&#x200B;이(가) 효과 레이어에 적용되고 *`fillOpacity`*&#x200B;은(는) 무시됩니다.

기본 레이어 컨텐츠의 유효한 불투명도는 ( *`opacity`* &#42; *`fillOpacity`* / 100)입니다. 효과 레이어의 유효한 불투명도는 (기본 *`opacity`* &#42; 효과 *`opacity`* / 100)입니다.

## 속성 {#section-ac3f136ff1584a2eab87500b7164f7fa}

레이어 속성입니다. `layer=comp`인 경우 현재 레이어 또는 합성 이미지에 적용됩니다.

## 기본값 {#section-abba67ed028049048ae43405ea69b164}

`opac=100,100`(레이어 불투명도가 변경되지 않음).

## 예 {#section-9710810e96af40538652e8ae4aadd3be}

... `&layer=1&text=variable%20opacity&opac=90,70&effect=-1&opac=50&`..

이 예제에서 텍스트 불투명도는 90&#42;70/100=63%이고 효과 레이어 불투명도는 90&#42;50/100=45%입니다.

## 참조 {#section-dbdad35ccd544590b4b11d31a9ab062e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)
