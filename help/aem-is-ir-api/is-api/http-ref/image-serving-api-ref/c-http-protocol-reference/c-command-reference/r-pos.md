---
description: 레이어 위치.
seo-description: 레이어 위치.
seo-title: pos
solution: Experience Manager
title: pos
topic: Scene7 Image Serving - Image Rendering API
uuid: e9872ce9-5c47-49c5-9c87-4fa8441c4770
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# pos{#pos}

레이어 위치.

pos= *`coord`*

posN= *`coordN`*

<table id="simpletable_754F76EE00BF4129B07502647FF172B7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>이 레이어의 원점을 레이어 0 원점(int, int)으로 픽셀 오프셋 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>이 레이어의 원점에서 레이어 0 원점으로 정규화된 오프셋(실제, 실제)을 만들 수 있습니다. </p></td> 
 </tr> 
</table>

이미지, 텍스트 및 단색 레이어의 경우 `pos=` 레이어 0 앵커를 기준으로 레이어 앵커의 위치를 지정합니다. `posN=` 좌표 값은 실제 레이어 0 rect 크기를 기준으로 표준화됩니다.

효과 레이어의 경우 `pos=` 효과 레이어를 상위 레이어를 기준으로 이동합니다.

양수 값을 지정하면 레이어를 오른쪽/아래쪽, 왼쪽/위쪽 방향으로 이동합니다. `posN=0.5,0.5` 레이어 0 폭과 높이를 두 배 정도 아래쪽과 오른쪽으로 이동합니다.

## 속성 {#section-51a60cdc52d040538fef378ace7c2e7d}

레이어 특성. 또는 인 경우 `layer=0` 무시됩니다 `layer=comp`.

## 기본값 {#section-70a6bc71ded5494e843194dfb6bf5a6c}

`posN=0,0`. 이렇게 하면 레이어 앵커가 이미지, 텍스트 또는 단색 레이어인 경우 레이어 0 앵커와 동일한 위치에 배치됩니다. 효과 레이어를 상위 레이어 바로 위나 아래에 배치할 수 있습니다.

## 예 {#section-a89a02c22f6b4260bfcf7c842cd6069d}

템플릿의 예 A를 [참조하십시오](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## 참조 {#section-812d95575ba542808e8387d0a8650606}

[origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)
