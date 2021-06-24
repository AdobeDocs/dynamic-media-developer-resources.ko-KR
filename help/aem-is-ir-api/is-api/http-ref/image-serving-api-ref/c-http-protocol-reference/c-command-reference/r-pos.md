---
description: 레이어 위치.
solution: Experience Manager
title: pos
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: c2e9a1f3-7216-4ab0-9c37-57f083119cef
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 3%

---

# pos{#pos}

레이어 위치.

pos= *`coord`*

posN= *`coordN`*

<table id="simpletable_754F76EE00BF4129B07502647FF172B7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 코드</span> </p> </td> 
  <td class="stentry"> <p>이 레이어의 원점에서 레이어 0 원점까지 픽셀 오프셋(int, int)입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>이 레이어의 원점에서 레이어 0 원점으로 정규화된 오프셋(실제, 실제)입니다. </p></td> 
 </tr> 
</table>

이미지, 텍스트 및 단색 레이어의 경우 `pos=` 은 레이어 0 앵커를 기준으로 레이어 앵커의 위치를 지정합니다. `posN=` 좌표 값은 실제 레이어 0 rect 크기를 기준으로 표준화됩니다.

효과 레이어의 경우 `pos=` 은 상위 레이어를 기준으로 효과 레이어를 이동합니다.

양수 값은 레이어를 오른쪽/아래쪽, 왼쪽/상단 방향으로 이동합니다. `posN=0.5,0.5` 레이어 0의 폭과 높이, 아래쪽과 오른쪽으로 레이어를 이동합니다.

## 속성 {#section-51a60cdc52d040538fef378ace7c2e7d}

레이어 속성입니다. `layer=0` 또는 `layer=comp`이면 무시됩니다.

## 기본값 {#section-70a6bc71ded5494e843194dfb6bf5a6c}

`posN=0,0`. 이렇게 하면 레이어 앵커가 이미지, 텍스트 또는 단색 레이어인 경우 레이어 0 앵커와 동일한 위치에 배치됩니다. 효과 레이어를 상위 레이어 위 또는 아래에 직접 배치합니다.

## 예 {#section-a89a02c22f6b4260bfcf7c842cd6069d}

[템플릿](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)의 예제 A 를 참조하십시오.

## 참조 {#section-812d95575ba542808e8387d0a8650606}

[원본=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)
