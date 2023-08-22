---
title: 크기
description: 레이어 크기. 회전=, 원근= 및 확장=을 레이어에 적용하기 전에 레이어의 크기 또는 최대 레이어 크기를 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 55feeb32-b69d-4b95-80fb-c77f2612d255
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 1%

---

# 크기{#size}

레이어 크기. 회전=, 원근= 및 확장=을 레이어에 적용하기 전에 레이어의 크기 또는 최대 레이어 크기를 지정합니다.

` size= *`폭`*, *`높이`*`

` sizeN= *`widthN`*, *`heightN`*`

<table id="simpletable_FBE17D736F93485AA0053BF447B4CC9F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 폭 </span>, <span class="varname"> 높이 </span> </span> </p> </td> 
  <td class="stentry"> <p>픽셀 단위 레이어 크기 제한(int, int, 0 이상). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> widthN </span>, <span class="varname"> heightN </span> </span> </p> </td> 
  <td class="stentry"> <p>레이어 0 크기(실수, 실수, 0.0...1.0)를 기준으로 정규화된 레이어 크기 제한입니다. </p> </td> 
 </tr> 
</table>

이미지 레이어에 대해 지정하면 size=는 레이어 이미지의 폭이나 높이 또는 두 가지 모두를 제한합니다. 이미지 크기가 보다 크지 않도록 조정되었습니다. `size=`. 정규화된 크기를 지정하면 레이어 0의 크기를 기준으로 합니다. 둘 다인 경우 *`width`* 및 *`height`* 을 지정하면 소스 이미지의 배율이 조정됩니다(다음 날짜 이후). `crop=` 두 차원이 지정된 크기를 초과하지 않도록 적용). 소스 사각형의 종횡비는 모든 경우에 유지됩니다. 다음 중 하나 *`width`* 또는 *`height`* 0으로 설정할 수 있습니다. 이 경우 서버는 이미지의 종횡비를 기반으로 값을 계산합니다.

텍스트 레이어에 지정된 경우 `size=` 텍스트 상자 크기를 지정합니다. *`width`* 은 필수입니다. *`height`* 0으로 설정할 수 있으며, 이 경우 배치된 텍스트의 높이가 레이어 높이로 사용됩니다. 기본적으로 텍스트 레이아웃 엔진은 텍스트가 항상 사용 가능한 공간에 수평으로 맞춰지도록 줄바꿈을 삽입합니다. If *`height`* 를 지정하면 사용 가능한 공간에 맞지 않는 선이 잘립니다( `text=`) 또는 생략됨( `textPs=`). `text=` 추가 맞춤 모드를 지원합니다. 다음을 참조하십시오. `textAttr=` 을 참조하십시오.

단색 레이어에 지정된 경우 `size=` 는 정확한 레이어 크기를 정의합니다. 마스크가 제공되지 않은 경우 두 값을 모두 지정해야 합니다. If `mask=` 또한 가 지정되면 마스크 이미지의 크기가 맞춰집니다 `size=` 이미지 레이어에서 이미지 크기를 조정하는 것과 동일한 방식입니다.

## 속성 {#section-5f254b66fcba49bcb63f9c9ea40b230c}

레이어 속성입니다. 다음과 같은 경우 레이어 0에 적용됩니다. `layer=comp`. `sizeN=` 다음에 대해 허용되지 않음 `layer=0` 또는 `layer=comp`. `sizeN=` 이(가) 다음에 대해 허용됩니다. `layer=0` 및 `layer=comp` 워터마크 이미지를 정의하는 카탈로그 레코드에서만 사용할 수 있습니다. 이 경우, `sizeN` 워터마크가 적용되는 합성 이미지를 기준으로 워터마크 이미지의 비율을 정의합니다. If `size=` 을(를) 지정했습니다. `res=` 및 `scale=` 이 레이어에 대해서는 무시됩니다. 효과 레이어에서 무시됨.

## 기본값 {#section-43d129deba6a441da66a1fdb63d1c85c}

`size=0,0`레이어 크기는 구속되지 않습니다. 이미지 레이어들에 대해, 그 다음, 레이어 크기는 임의의 이후에 레이어 이미지 크기에 기초하여 결정된다 `crop=`, `scale=`, 또는 `res=` 작업이 적용되었습니다. 텍스트 레이어의 경우 `size=` 를 지정하지 않으면 렌더링된 텍스트에 맞게 레이어의 크기가 자동으로 조정됩니다.

단색 레이어에는 완전히 지정된 색상 레이어가 필요합니다. `size=`, a `mask=`, 또는 `clipPath=`.

## 예 {#section-d1adaddd9e0b4ca881fd8e0a7541e5d9}

다음을 참조하십시오 [예 A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) 위치: [템플릿](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## 참조 {#section-63dfdf3750e249d2ab4c825ccd2e7181}

[scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065) , [res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [마스크=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [텍스트 레이어](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
